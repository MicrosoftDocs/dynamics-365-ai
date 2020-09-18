---
title: "Dynamics 365 Customer Service entities used by Customer Service Insights"
description: "Learn about the entities and attributes used by Customer Service Insights when a workspace is connected with Dynamics 365 Customer Service."
keywords: "CDS, data entity"
ms.date: 6/21/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Dynamics 365 Customer Service entities used by Customer Service Insights

When a workspace is created from a Dynamics 365 Customer Service environment, Customer Service Insights loads customer service data and generates dashboards using the following Dynamics 365 Customer Service entities:

- [Case entity](#case-entity)
- [CaseResolution entity](#caseresolution-entity)
- [BusinessUnit entity](#businessunit-entity)
- [Product entity](#product-entity)
- [User entity](#user-entity)
- [Team entity](#team-entity)

The following sections describe the entities and attributes used by Customer Service Insights.

## Case entity

The Case entity represents a service request case associated with a contract. Customer Service Insights generates dashboards using the following Case entity attributes:

Attributes | Type | Details
-----------|------|--------
IncidentId | UniqueIdentifier (Primary Key) | **Required.** A unique case identifier that is generated automatically when a case is created.
Title | String | A descriptive name that briefly summarizes the support issue or request. Customer Service Insights uses case titles to automatically group support cases into topics using natural language understanding technology. |
CreatedOn | DateTime | The date and time the case was created in common UTC time zone format.  
ModifiedOn | DateTime | The date and time the case was last modified in common UTC time zone format. If an [CaseResolution entity](#caseresolution-entity) is not available in the system, Customer Service Insights uses the value of the ModifiedOn attribute as the case resolution date and time.
IsEscalated | Boolean | **True** if the case has been escalated; otherwise, **False**.
EscalatedOn | DateTime | If a case was escalated, the date and time the case was escalated in common UTC time zone format.  
PriorityCode | Picklist | The case priority.
StateCode | State | **Required.** The case status. Customer Service Insights uses the following values to identify case status: **0** (Active), **1** (Resolved), **2** (Cancelled).
CaseOriginCode | Picklist | The support channel where the case originated.
ResolveBySLAStatus | Picklist | The status of the resolution time for the case according to the terms of the service level agreement (SLA). A value of 4 indicates a noncompliant case. Other values indicate the case complies with the SLA.
CustomerSatisfactionCode | Picklist | The customer's level of satisfaction with the handling and resolution of the case. Customer Service Insights uses the following values to indicate the level of satisfaction: **1** (Very Dissatisfied), **2** (Dissatisfied), **3** (Neutral), **4** (Satisfied), **5** (Very Satisfied).
OwningUser | Lookup | A unique identifier for the support agent who owns the case. Customer Service Insights uses this attribute to look up the agent name from the [User](#user-entity) entity and  generate agent performance charts on the [Case resolution dashboard](dashboard-case-resolutions.md) and [Topic details dashboard](dashboard-topic-details.md).
ProductId | Lookup | A unique identifier for the product associated with the case. Customer Service Insights uses this attribute to look up the product name from the [Product](#product-entity) entity and generate product information for the [Topic details dashboard](dashboard-topic-details.md) and the Product filter values on each dashboard.
OwningBusinessUnit | Lookup | A unique identifier for the business unit that owns the case. Customer Service Insights uses this attribute to look up the business unit names from the [BusinessUnit](#businessunit-entity) entity and generate the Business Unit filter values on each dashboard.
OwningTeam | Lookup | A unique identifier for the team that owns the case. Customer Service Insights uses this attribute to look up the team name from the [Team](#team-entity) entity and generate the Team filter values on each dashboard.
TicketNumber | String | The case number for customer reference and searching capabilities in a Dynamics 365 Customer Service environment. In Customer Service Insights, users can review cases grouped into each topic with their case numbers in the Topics page. 

For more information about the Case entity, see [Case Entity Reference](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/service/case).

## CaseResolution entity

The CaseResolution entity represents the activity when a case is resolved or reactivated. Customer Service Insights uses the CaseResolution entity to compute case resolution time. If the CaseResolution entity is not available in the system or no resolution record is found from the entity for a resolved case, Customer Service Insights uses the value of the ModifiedOn attribute in the [Case entity](#case-entity) as the case resolution date and time. Customer Service Insights uses the following attributes from the CaseResolution entity:

Attributes | Type | Details
-----------|------|--------
IncidentId | Lookup | A unique incident identifier.
CreatedOn | DateTime | The date and time the case resolution activity was created. Since a CaseResolution record is created when a case is resolved, this attribute indicates the date and time a case is resolved.
ModifiedOn | DateTime | The date and time the case resolution activity was last modified.
StateCode | Status | The case resolution status. Customer Service Insights uses the following values to indicate the status: 1 (Open), 2 (Completed), or 3 (Canceled). If a case is reactivated, Customer Service Insights updates the StateCode to 3 (Canceled). When the StateCode value is 2 (Completed), Customer Service Insights uses the value of the CreatedOn attribute as the case resolution date and time.

For more information about the CaseResolution entity, see [Case Resolution Entity Reference](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/service/caseresolution).

## BusinessUnit entity

The BusinessUnit entity represents a business, division, or department in the Microsoft Dynamics 365 database. Customer Service Insights uses the following BusinessUnit entity attributes.

Attributes | Type | Details
-----------|------|--------
BusinessUnitId | UniqueIdentifier (Primary Key) | A unique business unit identifier.
Name | String | The name of the business unit. Customer Service Insights uses this attribute to generate the Business Unit filter values on each dashboard.

For more information about the BusinessUnit entity, see [BusinessUnit Entity Reference](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/businessunit).

## Product entity

The Product entity represents information about products and their pricing information. Customer Service Insights uses the following attributes from the Product entity:

Attributes | Type | Details
-----------|------|--------
ProductId | UniqueIdentifier (Primary Key) | A unique product identifier.
Name | String | The name of the product. Customer Service Insights uses this attribute to generate the [Topic details dashboard](dashboard-topic-details.md) and the Product filter values on each dashboard.

For more information about the Product entity, see [Product Entity Reference](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/product).

## User entity

The User entity represents a person with access to the Microsoft CRM system who owns objects in the Microsoft CRM database. Customer Service Insights uses the following User entity attributes:

Attributes | Type | Details
-----------|------|--------
SystemUserId | UniqueIdentifier (Primary Key) | A unique identifier for the support agent.
FullName | String | The full name of the support agent. Customer Service Insights uses this attribute to generate agent performance charts on the [Case resolution dashboard](dashboard-case-resolutions.md) and [Topic details dashboard](dashboard-topic-details.md).

For more information about the User entity, see [User Entity Reference](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/service/user).

## Team entity

The Team entity represents a collection of system users that routinely collaborate. Customer Service Insights uses the following attributes from the Team entity:

Attributes | Type | Details
-----------|------|--------
TeamId | UniqueIdentifier (Primary Key) | A unique team identifier.
Name | String | The name of the team. Customer Service Insights uses this attribute to generate the Team filter values on each dashboard.

For more information about the Team entity, see [Team Entity Reference](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/team).
