## Cleaning up your Microsoft Azure Account

# Cleanup Operation

**First, what is a stale Device?** <br>
A stale device is one that has been registered with Azure AD but has not been used to access any cloud apps for an extended period of time.

To clear the entire environment, both AAD & Azure resources must be checked.

![Untitled design (3).png](https://cdn.hashnode.com/res/hashnode/image/upload/v1660316921234/8XjgUSyOA.png)
> It will be easier to find related resources if you inspect within the resource groups.

## Azure Active Directory Cleanup
### Prerequisites
The user must fit one of the responsibilities listed below in order to begin the cleaning procedure.

- Global Administrator
- Cloud Device Administrator
- Intune Service Administrator

### Timestamp
A timestamp is a string of characters or encoded information that indicates the time and date of an occurrence
Within the powershell it's also refered to: `ApproximateLastLogonTimestamp`

[This Hyperlink will take you to the device page](https://portal.azure.com/#blade/Microsoft_AAD_IAM/DevicesMenuBlade/Devices)

## Implementation Policy
You should establish a related **policy** in order to effectively remove outdated equipment from your environment.
With the aid of policy, you can make sure that you account for all factors associated to outdated technology.
> [Microsoft Docs on Stale device](https://docs.microsoft.com/en-us/azure/active-directory/devices/manage-stale-devices)


## Powershell to Cleanup Azure AD Stale Devices
Run Powershell as admin:
-  `Connect-MsolService`  : connect to the Azure AD tenant.
-  `Get-MsolDevice`: Get the list of devices
-  `Get-MsolDevice -all`: get all the device details without any filter.
-  `Get-MsolDevice -all | select-object -Property Enabled, DeviceId, DisplayName, DeviceTrustType, ApproximateLastLogonTimestamp | export-csv C:\devicelist-summary.csv`: stale devices to excel
-  `Disable-MsolDevice`: Disable Stale devices
-  `Remove-MsolDevice`: delete stale devices


---

## Azure Resources

In the case of unused resources,<br> we can delete them using an automated **powershell script**.


You must tag the resources with the **ExpiresOn tag** and then specify a **date** that is earlier than today.


``` 
$connectionName = "AzureRunAsConnection"
try
{
    # Get the connection "AzureRunAsConnection "
    $servicePrincipalConnection=Get-AutomationConnection -Name $connectionName         

    Connect-AzAccount `
        -ServicePrincipal `
        -Tenant $servicePrincipalConnection.TenantId `
        -ApplicationId $servicePrincipalConnection.ApplicationId `
        -CertificateThumbprint $servicePrincipalConnection.CertificateThumbprint 
}
catch {
    if (!$servicePrincipalConnection)
    {
        $ErrorMessage = "Connection $connectionName not found."
        throw $ErrorMessage
    } else{
        Write-Error -Message $_.Exception
        throw $_.Exception
    }
}

$expResources= Search-AzGraph -Query 'where todatetime(tags.expireOn) < now() | project id'

foreach ($r in $expResources) {
    Remove-AzResource -ResourceId $r.id -Force -WhatIf
}

$rgs = Get-AzResourceGroup;

foreach($resourceGroup in $rgs){
    $name=  $resourceGroup.ResourceGroupName;
    $count = (Get-AzResource | Where-Object{ $_.ResourceGroupName -match $name }).Count;
    if($count -eq 0){
        Remove-AzResourceGroup -Name $name -Force -WhatIf
    }
}

```

### Implementation
#### Import Modules
- Create an Azure Automation within the portal
- Give it a name, RG, Service principal default
- Once created, **Modules** within the left tab
- Browser Galery
- Import `az.accounts`
- Import `az.resourceGraph`
- Import `az.resources`

#### Create Runbooks
- Give it name
- Powershell Type
- Paste the script and click save
- Publish so we can use it
<br>

For automation: create a schedule, specify name, and start date.

Run the runbook to test if it worked.

> [Helpful Link!](https://dev.to/azure/keep-your-azure-subscription-clean-automatically-mmi) 

### NEXT
It is possible that you will experience an account that has been in a sleep mode for an extended period of time, as I did. So having a clearer vision of what to consider is a good first step. Good luck cleaning up the total mess. More research is required!