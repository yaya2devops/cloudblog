# On board to Sentinel And Defender

# Why Sentinel

Microsoft Sentinel is an innovative security solution that provides organizations with a comprehensive view of their cybersecurity posture. It leverages the power of cloud computing to provide real-time threat detection and response capabilities, allowing companies to stay ahead of malicious actors and protect their data from being compromised. With its advanced analytics, machine learning algorithms, automated incident response workflows, and integrated reporting features, Microsoft Sentinel helps organizations gain visibility into threats across the entire enterprise so they can act quickly when needed.

It also offers powerful automation capabilities for responding swiftly when incidents do occur—allowing teams more time for proactive measures instead of reactive ones and providing better insights into what happened after an attack occurred so appropriate countermeasures can be taken moving forward..

## Touchpoints

Azure Sentinel is a cloud-native SIEM & SOAR solution that collects data from multiple sources to provide a comprehensive picture of what is going on in your organization.

*   Sentinel is a **SIEM** (Security Information and Event Management)  
    Investigate, Find threats, Incidents, alerts..
    
*   Sentinel is a **SOAR** (Security Orchestration automation response tool)  
    Reacting to SIEM.
    

**SIEM** Find Things  
**SOAR** Do Something About it

## Architecture

![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659465636763/4-lE0GdpO.png)

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

# Defender

Azure Defender (CSPM) can be thought of as an upgrade to Azure Security Center (ASC), a dashboard available in the Azure portal that provides an overview of all of your assets in Azure and non-Azure environments, as well as a set of scores and recommendations to properly secure them.

![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1659465659404/5U1XS1SvK.png)

Microsoft Sentinel and Defender are two of the most powerful cybersecurity tools available today. They both provide advanced protection against a variety of cyber threats, such as malware, ransomware, phishing scams and more. With their comprehensive suite of features and capabilities, they can help organizations protect themselves from malicious attacks while also providing them with valuable insights into their security posture.

The integration between Azure Sentinel and Defender enables users to access all their security events from one single platform without needing multiple tools for different tasks. This makes it easier for IT teams to identify potential threats across multiple systems at once while reducing costs associated with purchasing additional products or services separately. Additionally, this helps improve overall visibility into an organization's environment so they can respond faster when suspicious activity occurs.

> [Connect Microsoft Defender for Cloud alerts to Microsoft Sentinel](https://docs.microsoft.com/en-us/azure/sentinel/connect-defender-for-cloud)

Defender comes in a variety of flavors depending on the application; some of them are listed below.

*   Microsoft Defender for Cloud (Azure Security Center)
    
*   Microsoft Defender for Office 365
    
*   Microsoft Defender for Identity
    
*   Microsoft Defender for Endpoint
    

> [Microsoft Defender for Cloud pricing](https://azure.microsoft.com/en-us/pricing/details/defender-for-cloud/)

Your first step should be with connecting to the data sources that you require. Give it at least 60 minutes.

* * *

# Conclude

Microsoft Sentinal is a great tool for any organization looking for improved cybersecurity protection while still maintaining control over its IT environment without sacrificing performance or scalability needs! Just care about the costs!

Furthermore, integrating Azure Sentinel and Defender offers organizations a powerful combination that enhances their ability to protect against cyber attacks.
