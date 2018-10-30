---
title: " Dynamics 365 AI for Sales capabilities for sellers Privacy Notices | Microsoft Docs"
description: "Privacy notices for AI for Sales capabilities for sellers."
keywords: "privacy notice, privacy statement addition"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 06d7fae8-8332-43ce-bd9c-d52b9a3041d2
author: udaykirang
ms.author: udag
manager: shujoshi
ms.custom: dyn365-ai-sales
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Dynamics 365 AI for Sales capabilities for sellers privacy notices

Your privacy is important to us. For Microsoft Online Services, read the [Microsoft Online Services privacy Statement](https://go.microsoft.com/fwlink/p/?LinkID=389041).

For specific privacy information about Dynamics 365 AI for Sales capabilities for sellers, refer to the paragraphs below.

By enabling [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] capabilities, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Data will be sent to and used by (1) Azure Data Factory for the purpose of data movement and transformation for KPI computation, and (2) Azure Container Instance for the purpose of predictive model training and scoring. By installing this solution, you agree for this limited set of data to be sent to Azure Data Factory service and Azure Container Instance.

Azure components and services that are involved with Dynamics 365 AI for Sales are detailed in the following sections.
[!Include[cc_privacy_note_azure_trust_center](../includes/cc-privacy-note-azure-trust-center.md)]

## Azure Data Factory
[!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] uses Azure Data Factory, a cloud data integration service, to orchestrate and automate the movement and transformation of data (including Customer Data) between services.

## Azure Container Instance
[!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] uses Azure Container instance, a cloud-based container service, to create predictive model training and scoring pipelines dynamically. 

## Installation and Removal of Dynamics 365 AI for Sales

An administrator can enable [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] embedded capabilities by installing it as a solution in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization. In addition, an administrator can subsequently disable the feature by uninstalling this solution from the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization.



### See also

- [Configure and enable AI for sales](configure-enable-sales-insights-addon.md)
- [Use Relationship analytics to gather KPIs](relationship-analytics.md)
- [Prioritize leads through scores](work-predictive-lead-scoring.md) 
- [Prioritize opportunities through scores](work-predictive-opportunity-scoring.md)
- [How notes analysis assists you with suggestion](notes-analysis.md)
- [Know conversation starters for your customers](talking-points.md)
- [How to get introduced to a lead](who-knows-whom.md)