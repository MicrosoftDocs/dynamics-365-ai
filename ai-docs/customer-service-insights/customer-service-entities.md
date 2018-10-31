---
title: "Dynamics 365 for Customer Service entities used by Customer Service Insights"
description: "Learn about the default data entities and attributes used by Customer Service Insights when a workspace is connected with Dynamics 365."
keywords: "CDS, data entity"
ms.date: 10/30/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: gxy001
ms.author: gxy001
manager: ankitsar
---

# Dynamics 365 for Customer Service entities used by Customer Service Insights

When a workspace is created from a Dynamics 365 environment, Customer Service Insights loads the customer service data stored in Dynamics 365/Common Data Service (CDS) from the following entities to generate dashboards:

- [Incident (case)](#BKMK_incident_entity)
- [BusinessUnit](#BKMK_businessunit_entity)
- [Product](#BKMK_product_entity)
- [SystemUser](#BKMK_systemuser_entity)
- [Team](#BKMK_team_entity)

## <a name="BKMK_incident_entity"></a> Incident (case) entity
Customer Service Insights uses the following attributes from Incident entity to generate dashboards. You can find more details about this entity from [Incident (case) Entity Reference](https://docs.microsoft.com/dynamics365/customer-engagement/developer/entities/incident).

Attributes | Type | Details
-----------|------|--------
IncidentId | UniqueIdentifier <br> (Primary Key) | **System required.** Unique identifier of the case that is auto-generated when a case is created. 
Title | String | A descriptive name that briefly summarize the support issue or request. <br><br> Customer Service Insights uses case titles to automatically group cases into topics using natural language understanding. | 
CreatedOn | DateTime | Date and time when the case was created. The values are returned using a common UTC time zone format.  
ModifiedOn | DateTime | Date and time when the case was last modified. The values are returned using a common UTC time zone format.  
IsEscalated | Boolean | Indicates if the case has been escalated.
EscalatedOn | DateTime | Indicates the date and time when the case was escalated. The values are returned using a common UTC time zone format.  
PriorityCode | Picklist | Indicates the case priority. <br><br> Customer Service Insights takes the following numeric values to identify priorities. Other values will show as Custom on the dashboards. <br><br> **Value**	(Priority): <br><li> **1** 	(High) <br><li> **2**	(Medium) <br><li> **3**	(Low)
StateCode | State | **System required.** Indicates the case status. <br><br>Customer Service Insights takes the following numeric values to identify case status: <br><br> **Value** (Status): <br><li> **0** (Active) <br><li> **1** (Resolved) <br><li> **2** (Cancelled)
CaseOriginCode | Picklist | Indicates the support channel where the case was originated. <br><br> Customer Service Insights takes the following numeric value to report different support channels: <br><br> **Value** (Support Channel): <br><li> **1** (Phone) <br><li> **2** (Email) <br><li> **3** (Web) <br><li> **2483** (Facebook) <br><li> **3986** (Twitter)
ResolveBySLAStatus | Picklist | Shows the status of the resolution time for the case according to the terms of the SLA. <br><br> This is the key data field for Customer Service Insights to report statistics of SLA compliant cases. <br><br> Customer Service Insights checks whether the value equals to 4, which indicate a noncompliant case. Other values are treated as compliant. 
CustomerSatisfactionCode | Picklist | Indicate customers’ level of satisfaction with the handling and resolution of the case. <br><br> This is the key data field for Customer Service Insights to report statistics of customer satisfaction (CSAT). <br><br> Customer Service Insights reads the following values for different levels of satisfaction: <br><br> **Value**  (Satisfaction level): <br><li> **1** (Very Dissatisfied) <br><li> **2** (Dissatisfied) <br><li> **3** (Neutral) <br><li> **4** (Satisfied) <br><li> **5** (Very Satisfied)
OwningUser | Lookup | Unique identifier for the support agent that owns the case. Customer Service Insights uses this field to look up agent full names from [SystemUser](#BKMK_systemuser_entity) entity. <br><br> The data are aggregated to generate agent performance charts in [case resolution dashboard](dashboard-case-resolutions.md) and [topic details dashboard](dashboard-topic-details.md). 
ProductId | Lookup | Unique identifier that indicates the product associated with the case. Customer Service Insights uses this field to look up product names from [Product](#BKMK_product_entity) entity. <br><br> The data are aggregated to generate [topic details dashboard](dashboard-topic-details.md) and the Product filter on each dashboard.
OwningBusinessUnit | Lookup | Unique identifier for the business unit that owns the case. Customer Service Insights uses this field to look up business unit names from [BusinessUnit](#BKMK_businessunit_entity) entity. <br><br> The data are aggregated to generate the Business Unit filter on each dashboard.
OwningTeam | Lookup | Unique identifier for the team that owns the case. Customer Service Insights uses this field to look up team names from [Team](#BKMK_team_entity) entity. <br><br> The data are aggregated to generate the Team filter on each dashboard.

## <a name="BKMK_businessunit_entity"></a> BusinessUnit entity
Customer Service Insights uses the following attributes from BusinessUnit entity. You can find more details about this entity from [BusinessUnit Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/businessunit).

Attributes | Type | Details
-----------|------|--------
BusinessUnitId | UniqueIdentifier <br> (Primary Key) | Unique identifier of the business unit.
Name | String | Name of the business unit. The data are aggregated to generate the Business Unit filter on each dashboard.

## <a name="BKMK_product_entity"></a> Product entity
Customer Service Insights uses the following attributes from Product entity. You can find more details about this entity from [Product Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/product).

Attributes | Type | Details
-----------|------|--------
ProductId | UniqueIdentifier <br> (Primary Key) | Unique identifier of the product.
Name | String | Name of the product. The data are aggregated to generate [topic details dashboard](dashboard-topic-details.md) and the Product filter on each dashboard.

## <a name="BKMK_systemuser_entity"></a> SystemUser entity
Customer Service Insights uses the following attributes from SystemUser entity. You can find more details about this entity from [SystemUser Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/systemuser).

Attributes | Type | Details
-----------|------|--------
SystemUserId | UniqueIdentifier <br> (Primary Key) | Unique identifier for the support agent.
FullName | String | Full name of the support agent. The data are aggregated to generate agent performance charts in [case resolution dashboard](dashboard-case-resolutions.md) and [topic details dashboard](dashboard-topic-details.md). 


## <a name="BKMK_team_entity"></a> Team entity
Customer Service Insights uses the following attributes from Team entity. You can find more details about this entity from [Team Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/team).

Attributes | Type | Details
-----------|------|--------
TeamId | UniqueIdentifier <br> (Primary Key) | Unique identifier for the team.
Name | String | Name of the team. The data are aggregated to generate the Team filter on each dashboard.

