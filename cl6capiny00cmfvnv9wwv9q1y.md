# Azure Cloud Security | Sentinel And Defender
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1659451510570/GigxwP0Dd.gif?w=1600&h=840&fit=crop&crop=entropy&auto=format,compress&gif-q=60&format=webm">

# Microsoft Sentinel

## Overview
Azure Sentinel is a cloud-native SIEM & SOAR solution that collects data from multiple sources to provide a comprehensive picture of what is going on in your organization.

- Sentinel is a **SIEM** (Security Information and Event Management)
<br>👉 Investigate, Find threats, Incidents, alerts..
- Sentinel is a **SOAR** (Security Orchestration automation response tool) <br>👉Reacting to SIEM.

**SIEM**👉 Find Things <br>
**SOAR**👉 Do Something About it


## Architecture

![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659465636763/4-lE0GdpO.png)



 Sentinel is built on top of an analytics workspace, with a machine learning layer added (Intelligence Threat) to investigate and find things clearly and meaningfully in these massive amounts of data. 



## Core components

### 1- Data Connectors
Data connectors are responsible for managing the libraries and configurations required for hosts to connect to various data sources. A data connector includes the type, URI, authentication method, and all libraries required to access the data source.
> [Enable a Data Connector](https://docs.microsoft.com/en-us/azure/sentinel/connect-data-sources#enable-a-data-connector)

### 2- Analytics (Rules)
Analytics rules scan your environment for certain events or groups of events, notify you when particular event thresholds or criteria are met, create incidents for your SOC to analyze and triage, and respond to threats with automated monitoring and remediation procedures.
> You can select from a variety of assault categories in the Tactics and tactics field to categorize the rule. These are based on the MITRE ATT&CK framework's strategies and tactics.


### 3- Playbooks ( for automation)
Takes you to create a custom LogicApp.
Or you can relay on the [sentinel repo](https://github.com/Azure/Azure-Sentinel) to find a template and do the a logicapp for you.
### 4- WorkBooks
Workbooks have a wide range of applications, from simple data presentation to complex graphing and resource investigation maps.

### 5- Hunting (look for something)
 **Query and get insights using KQL**
  Run the desired KQL and get results to improve your insights on the data.
  <br>
  
### 6- Notebooks
 **Query and get insights using ML**
Built on top of Jupiter Notebooks, a pattern to look for things, security informations.
Write machine learning in various programming languages such as Python.


> [Sentinel Pricing](https://azure.microsoft.com/fr-fr/pricing/details/microsoft-sentinel/)

---

# Scenarios
- Use **Azure Event Hub** to **Continuous export of high severity alerts and retrieval from 3rd party SIEM solution**


- Use Diagnostics settings in azure AD and stream to an event hub **to Generate alerts from Azure Active Directory**


---
# Defender

![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659465659404/5U1XS1SvK.png)

Azure Defender (CSPM) can be thought of as an upgrade to Azure Security Center (ASC), a dashboard available in the Azure portal that provides an overview of all of your assets in Azure and non-Azure environments, as well as a set of scores and recommendations to properly secure them.

**Azure Sentinel** includes a wide range of data connectors. Among them is Azure Defender.

Defender comes in a variety of flavors depending on the application; some of them are listed below.
- Microsoft Defender for Cloud (Azure Security Center)
- Microsoft Defender for Office 365
- Microsoft Defender for Identity
- Microsoft Defender for Endpoint

> [Microsoft Defender for Cloud pricing](https://azure.microsoft.com/en-us/pricing/details/defender-for-cloud/)

---
# Project: EventHub
> Sending logs and establishing monitoring use cases with Sentinel/Defender.

**Decision tree**: Determine how many workspaces are required for this project **❓**

![](https://i.imgur.com/jSOvhdP.jpg)

---

## The Objective 🥅


### A: Send logs to Sentinel

#### Sentinel Migration:
![](https://i.imgur.com/Y0sfQYZ.png)

**Tasks:**

#### Task1📝:
- Configuring log ingestion from **Sharepoint**
- Putting the ingestion into production and validating the correlation of the logs. 
 <br><br>
- Configuring log ingestion from **Teams**
- Putting the ingestion into production and validating the correlation of the logs.
<br><br>
> [Monitor Logs from Azure Sentinel (Sharepoint, Teams)](https://nanddeepnachanblogs.com/posts/2021-03-14-monitor-o365-logs-azure-sentinel/)

---
#### Task2📝:
- Configuring log ingestion from **Dynamics 365 Sales**
- Putting the ingestion into production and validating the correlation of the logs.
<br><br>
- Configuring log ingestion from **Power Apps**
- Putting the ingestion into production and validating the correlation of the log.

> [Office 365 Management API data into Azure Sentinel](https://github.com/Azure/Azure-Sentinel/tree/master/DataConnectors/O365%20Data)

---
#### Task3📝:
- Configuring log ingestion from **AAD**
- Putting the ingestion into production and validating the correlation of the logs.
<br><br>
- Configuring log ingestion from **Azure SQL Managed Instance**
- Putting the ingestion into production and validating the correlation of the logs.
<br><br>


### B: Develop surveillance use cases

> [SIEM – USE CASE WRITING GUIDE]()
Consult the **[MITRE ATT&CK® framework](https://resources.infosecinstitute.com/topic/use-cases-for-implementing-the-mitre-attck-framework/).** <br>

>I'd been debating a color for this one **for a while** and couldn't come up with anything creative, haha,  I'm including it anyway.
![Renew & Stay Certified (17).gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1660780135878/drH9_17ZN.gif)
