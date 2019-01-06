---
title: "Dynamics 365 for Customer Service entities used by AI for Customer Service Insights"
description: "Learn about the entities and attributes used by AI for Customer Service Insights when a workspace is connected with Dynamics 365 for Customer Service."
keywords: "CDS, data entity"
ms.date: 10/31/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Dynamics 365 for Customer Service entities used by AI for Customer Service Insights

When a workspace is created from a Dynamics 365 for Customer Service environment, AI for Customer Service Insights loads customer service data and generates dashboards using the following Dynamics 365 for Customer Service entities:

- [Incident (case)](#incident-case-entity)
- [BusinessUnit](#businessunit-entity)
- [Product](#product-entity)
- [SystemUser](#systemuser-entity)
- [Team](#team-entity)

The following sections describe the entities and attributes used by AI for Customer Service Insights.

## Incident (case) entity

The Incident (case) entity represents a service request case associated with a contract. AI for Customer Service Insights generates dashboards using the following Incident (case) entity attributes:

Attributes | Type | Details
-----------|------|--------
IncidentId | UniqueIdentifier (Primary Key) | **Required.** A unique case identifier that is generated automatically when a case is created.
Title | String | A descriptive name that briefly summarizes the support issue or request.  AI for Customer Service Insights uses case titles to automatically group support cases into topics using natural language understanding technology. |
CreatedOn | DateTime | The date and time the case was created in common UTC time zone format.  
ModifiedOn | DateTime | The date and time the case was last modified in common UTC time zone format.  
IsEscalated | Boolean | **True** if the case has been escalated; otherwise, **False**.
EscalatedOn | DateTime | If a case was escalated, the date and time the case was escalated in common UTC time zone format.  
PriorityCode | Picklist | The case priority.
StateCode | State | **Required.** The case status. AI for Customer Service Insights uses the following values to identify case status: **0** (Active), **1** (Resolved), **2** (Cancelled).
CaseOriginCode | Picklist | The support channel where the case originated.
ResolveBySLAStatus | Picklist | The status of the resolution time for the case according to the terms of the service level agreement (SLA). A value of 4 indicates a non-compliant case. Other values indicate the case complies with the SLA.
CustomerSatisfactionCode | Picklist | The customer's level of satisfaction with the handling and resolution of the case. Customer Service Insights uses the following values to indicate the level of satisfaction: **1** (Very Dissatisfied), **2** (Dissatisfied), **3** (Neutral), **4** (Satisfied), **5** (Very Satisfied).
OwningUser | Lookup | A unique identifier for the support agent who owns the case. AI for Customer Service Insights uses this attribute to look up the agent name from the [SystemUser](#systemuser-entity) entity and  generate agent performance charts on the [Case resolution dashboard](dashboard-case-resolutions.md) and [Topic details dashboard](dashboard-topic-details.md).
ProductId | Lookup | A unique identifier for the product associated with the case. AI for Customer Service Insights uses this attribute to look up the product name from the [Product](#product-entity) entity and generate product information for the [Topic details dashboard](dashboard-topic-details.md) and the Product filter values on each dashboard.
OwningBusinessUnit | Lookup | A unique identifier for the business unit that owns the case. AI for Customer Service Insights uses this attribute to look up the business unit names from the [BusinessUnit](#businessunit-entity) entity and generate the Business Unit filter values on each dashboard.
OwningTeam | Lookup | A unique identifier for the team that owns the case. AI for Customer Service Insights uses this attribute to look up the team name from the [Team](#team-entity) entity and generate the Team filter values on each dashboard.

For more information about the Incident (case) entity, see [Incident (case) Entity Reference](https://docs.microsoft.com/dynamics365/customer-engagement/developer/entities/incident).

## BusinessUnit entity

The BusinessUnit entity represents a business, division, or department in the Microsoft Dynamics 365 database. AI for Customer Service Insights uses the following  BusinessUnit entity attributes.

Attributes | Type | Details
-----------|------|--------
BusinessUnitId | UniqueIdentifier (Primary Key) | A unique business unit identifier.
Name | String | The name of the business unit. AI for Customer Service Insights uses this attribute to generate the Business Unit filter values on each dashboard.

For more information about the BusinessUnit entity, see [BusinessUnit Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/businessunit).

## Product entity

The Product entity represents information about products and their pricing information. AI for Customer Service Insights uses the following attributes from the Product entity:

Attributes | Type | Details
-----------|------|--------
ProductId | UniqueIdentifier (Primary Key) | A unique product identifier.
Name | String | The name of the product. AI for Customer Service Insights uses this attribute to generate the [Topic details dashboard](dashboard-topic-details.md) and the Product filter values on each dashboard.

For more information about the Product entity, see [Product Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/product).

## SystemUser entity

The SystemUser entity represents a person with access to the Microsoft CRM system who owns objects in the Microsoft CRM database. AI for Customer Service Insights uses the following SystemUser entity attributes:

Attributes | Type | Details
-----------|------|--------
SystemUserId | UniqueIdentifier (Primary Key) | A unique identifier for the support agent.
FullName | String | The full name of the support agent. AI for Customer Service Insights uses this attribute to generate agent performance charts on the [Case resolution dashboard](dashboard-case-resolutions.md) and [Topic details dashboard](dashboard-topic-details.md).

For more information about the SystemUser entity, see [SystemUser Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/systemuser).

## Team entity

The Team entity represents a collection of system users that routinely collaborate. AI for Customer Service Insights uses the following attributes from the Team entity:

Attributes | Type | Details
-----------|------|--------
TeamId | UniqueIdentifier (Primary Key) | A unique team identifier.
Name | String | The name of the team. AI for Customer Service Insights uses this attribute to generate the Team filter values on each dashboard.

For more information about the Team entity, see [Team Entity Reference](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/entities/team).
