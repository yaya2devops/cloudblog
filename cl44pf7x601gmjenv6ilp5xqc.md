## Cost Management and Cloud Migration | Microsoft Azure Edition




# Brief
When shifting to the cloud, one of the most crucial things to keep in mind is how to better manage your resources and spend as little money as possible.
It's self-evident that using the cloud rather than on-premise technology can save you a large sum of cash.
There are, however, numerous practices that I will list from which you can benefit in order to reduce your costs and spend more wisely.

# Cost Estimation
Before deploying any resources, the first step in answering our query is to estimate.
These set of tools would be useful prior to a cloud migration.

- [Total Cost of Ownership (TCO) Calculator:](https://azure.microsoft.com/en-us/pricing/tco/calculator/) To estimate the savings of the desired solution versus on-premise. You can enter what you're currently using into the TCO Calculator and have it convert it to Azure equivalent.
- [Azure Pricing calculator:](https://azure.microsoft.com/fr-fr/pricing/calculator/)
When you know exactly what you need in Azure and want to look up the price for resources that you already have.

---

# Azure Cost Management + Billing
Azure Cost Management + Billing is a multi-cloud pricing management service that aides you in making the best use and control of Azure and other cloud resources including AWS and GCP.

## Cost analysis
Cost analysis is a feature of Azure Cost Management that allows you to see total costs over time. This view might facilitate you in comprehending your spending patterns.

![costsana.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654637990371/JRa_yvM9U.png)
If you want to know how much a service costs right now, or if you're attempting to find out why your bill is greater than you expected, this is the tool to utilize.

## Azure Advisor 
A sophisticated tool that gives you environmental advice based on your goals, as well as information on how to improve, save money, expand availability, and safeguard your environment. 

![Azure-Advisor-Recommendations.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1654638337828/EsD11TO-q.jpg)
## Budget
This allows you to create custom cost and usage budgets and receive notifications when those budgets are crossed.
An Azure subscription budget can be created for a monthly, quarterly, or annual period.

> What about a notification by email, for example? ⬇️

### Alerts
Alerts warn you when your expenditure reaches or surpasses the amount specified in the budget's alert condition based on consumption or cost.

## Power BI Intergration
With the Azure Cost Management connector for Power BI Desktop, you can create powerful, customized visualizations and reports to better understand your Azure spending.


> Log in to your Power Apps and get data as shown below
![azure-cost-management-00b.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1654638943794/p_QKucQjb.png)


---

# Cost-Influencing 
Factors to consider when utilizing Azure that may affect the price.
 ### Subscription 
There are three main types of subscriptions available, **free, pay-as-you-go, and member offers**.
> It's necessary to think about each one in terms of your requirements.

 ### Azure Reservations
By committing to one-year or three-year agreements for several products, Azure Reservations can help you save money. You can get a discount on the resources you use if you commit. When compared to pay-as-you-go charges, reservations can save you up to 70 % on your resource costs.

 ### Resource Type & Usage
When a large quantity of cpu is operating, one of the most important variables in the price is the service; some services are free, while others pay a lot. Likewise the duration of the service should be something to regard.

### Locations & Regions
Azure products have different prices depending on you deploy them. If at all possible, use them in locations and regions where they are less expensive.

---

# Scenarios
### Carry AWS Expenses
Yes, you can track the costs of a different cloud provider, such as AWS, and bring them into Azure by establishing a [connector](https://docs.microsoft.com/en-us/azure/cost-management-billing/costs/aws-integration-set-up-configure).

### Existent Report System
To gain automated access to Azure resource cost and usage data. 
<br> [Azure Consumption API](https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/consumption-api-overview) can be used.


### Export Capability
This [feature](https://docs.microsoft.com/en-us/azure/cost-management-billing/costs/tutorial-export-acm-data?tabs=azure-portal) allows you to submit billing data to the Storage service on a monthly or weekly basis.


---


# Summary
The possibilities and methods used to optimize costs are endless. There's always something new to benefit from. However, adopting certain best practices for utilizing these novel technologies would undoubtedly aid us in optimizing and progressing.












