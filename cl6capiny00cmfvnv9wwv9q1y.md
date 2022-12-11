# Cloud Security | Sentinel And Defender

# Microsoft Sentinel

## Overview

Azure Sentinel is a cloud-native SIEM & SOAR solution that collects data from multiple sources to provide a comprehensive picture of what is going on in your organization.

*   Sentinel is a **SIEM** (Security Information and Event Management)  
    Investigate, Find threats, Incidents, alerts..
    
*   Sentinel is a **SOAR** (Security Orchestration automation response tool)  
    Reacting to SIEM.
    

**SIEM** Find Things  
**SOAR** Do Something About it

## Architecture

![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659465636763/4-lE0GdpO.png align="left")

Sentinel is built on top of an analytics workspace, with a machine learning layer added (Intelligence Threat) to investigate and find things clearly and meaningfully in these massive amounts of data.

## Core components

### Data Connectors

Data connectors are responsible for managing the libraries and configurations required for hosts to connect to various data sources. A data connector includes the type, URI, authentication method, and all libraries required to access the data source.

> [Enable a Data Connector](https://docs.microsoft.com/en-us/azure/sentinel/connect-data-sources#enable-a-data-connector)

### Analytics (Rules)

Analytics rules scan your environment for certain events or groups of events, notify you when particular event thresholds or criteria are met, create incidents for your SOC to analyze and triage, and respond to threats with automated monitoring and remediation procedures.

> You can select from a variety of assault categories in the Tactics and tactics field to categorize the rule. These are based on the MITRE ATT&CK framework's strategies and tactics.

### Playbooks ( for automation)

Takes you to create a custom LogicApp. Or you can relay on the [sentinel repo](https://github.com/Azure/Azure-Sentinel) to find a template and do the a logicapp for you.

### WorkBooks

Workbooks have a wide range of applications, from simple data presentation to complex graphing and resource investigation maps.

### Hunting (look for something)

**Query and get insights using KQL** Run the desired KQL and get results to improve your insights on the data.

### Notebooks

**Query and get insights using ML** Built on top of Jupiter Notebooks, a pattern to look for things, security informations. Write machine learning in various programming languages such as Python.

> [Sentinel Pricing](https://azure.microsoft.com/fr-fr/pricing/details/microsoft-sentinel/)

[Implement Sentinel Now](https://sentinel.yahya-abulhaj.dev/)

* * *

# Scenarios

*   Use **Azure Event Hub** to **Continuous export of high severity alerts and retrieval from 3rd party SIEM solution**
    
*   Use Diagnostics settings in azure AD and stream to an event hub **to Generate alerts from Azure Active Directory**
    

* * *

# Defender

![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659465659404/5U1XS1SvK.png align="left")

Azure Defender (CSPM) can be thought of as an upgrade to Azure Security Center (ASC), a dashboard available in the Azure portal that provides an overview of all of your assets in Azure and non-Azure environments, as well as a set of scores and recommendations to properly secure them.

**Azure Sentinel** includes a wide range of data connectors. Among them is Azure Defender.

> [Connect Microsoft Defender for Cloud alerts to Microsoft Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/connect-defender-for-cloud)

Defender comes in a variety of flavors depending on the application; some of them are listed below.

*   Microsoft Defender for Cloud (Azure Security Center)
    
*   Microsoft Defender for Office 365
    
*   Microsoft Defender for Identity
    
*   Microsoft Defender for Endpoint
    

> [Microsoft Defender for Cloud pricing](https://azure.microsoft.com/en-us/pricing/details/defender-for-cloud/)

Your first step should be with connecting to the data sources that you require. Give it atleast 60 minutes in order to start hunting and looking for insights on the workbooks created.

Honestly, Sentinel is a really powerfull tool for anyone wishing to get more aware and improve his/her work ethics along the way.

* * *

> I'd been debating a color for this one **for a while** and couldn't come up with anything creative, haha, I'm including it anyway.