---
title: "Configure and enable Sales Insights add-on for Dynamics 365 for Customer Engagement | MicrosoftDocs"
description: "Configure and enable Sales insights add-on"
keywords: "sales insights addon, insights addon, relationship analytics, predictive lead scoring, lead scoring"
ms.date: 10/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 93676b52-d168-497d-957f-ae2c8627645a
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 1
topic-status: Drafting
---

# Enable and configure Dynamics 365 Sales Inisghts capabilities for sellers

<!--Applies to [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] (online), version 9.1.0-->

> [!IMPORTANT]
> - Dynamics 365 Sales Insights capabilities for sellers requires [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] 9.1.0.35 and above.
> - The feature **Who knows who** and exchange data for **Relationship analytics** are available only in North American (NAM) regions.

Enabling and configuring the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] features helps the user to effectively use the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)]. The [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] contains the following features:

- Relationship analytics
- Predictive lead scoring
- Predictive opportunity scoring
- Notes analysis
- Talking points
- Who knows whom  


## GDPR

To learn about [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] related **General Data Protection Regulation (GDPR)**, see [Dynamics 365 Sales Insights and GDPR](embedded-intelligence-gdpr.md).

## Prerequisites

Review the following requirements before you enable and configure the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] feature:

- You must purchase a **Dynamics 365 Sales Insights** license to use [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] features.
- You must be a [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] administrator.
- Exchange email server is configured, and mailbox is enabled using **Email Configurations** in Settings. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [System Settings dialog box - Email tab](/dynamics365/customer-engagement/admin/system-settings-dialog-box-email-tab).
- If you want to use LinkedIn data for Relationship analytics, verify that the LinkedIn solution is installed in [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] and write back from LinkedIn Sales navigator is enabled.

## Enable Dynamics 365 Sales Insights features

[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] features are not available by default. You must enable these features by selecting an organization. Follow these steps:

1. Go to **Settings** > **Sales AI**.<br>
1. On the **AI setup** page, select **Get it now**.<br>
    > [!div class="mx-imgBorder"]
    > ![Get Dynamics 365 Sales Insights](media/d365-ai-sales-getitnow.png "Get Dynamics 365 Sales Insights")<br>
1. On the **Sales Insights** installation page, carefully read and select the terms and conditions, and then select **Continue**.<br>
   The installation takes a few minutes to complete, and then the status appears in the status bar.<br>
    > [!div class="mx-imgBorder"]
    > ![Accept Sales Insights add-on terms and conditions](media/sales-insights-addon-terms-conditions.png "Accept Sales Insights add-on terms and conditions")
   
    Status of installation is displayed. When complete, you're ready to configure [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] features.
    
    > [!div class="mx-imgBorder"]
    > ![Dynamics 365 Sales Insights is enabled](media/sales-insights-addon-enabled.png "Dynamics 365 Sales Insights is enabled")

## Privacy notice  

For specific privacy information about Dynamics 365 Sales Insights capabilities for sellers, see [Privacy notice](privacy-notice-seller.md).

### See also

- [Opt out of relationship analytics (GDPR)](optout-relationship-analytics-gdpr.md)
- [GDPR for Sales insights add-on](embedded-intelligence-gdpr.md)
- [View and export KPI data (GDPR)](view-export-KPI-data-gdpr.md)
- [Retrieve insights data using msdyn_RetrieveTypeValuesFromDCI action](retrieve-insights-data-msdyn-RetrieveTypeValuesFromDCI.md)
