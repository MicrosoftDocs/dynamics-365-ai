---
title: "Configure Relationship analytics for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure Relationship analytics for Sales Insights"
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 03bfdad0-2575-4c4b-a845-d7ac1ff0b0c3
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Configure Relationship analytics

Relationship analytics provides graphical representation of KPIs and activity histories for any contact, opportunity, lead or account to the users. 

To configure Relationship analytics, follow these steps:

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features) 

2. Go to **Change area** and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3. On the sitemap, select **Relationship analytics** under **Connection insights**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Manage** from the **Relationship analytics** section to go to configuration page.

    The configuration page opens.

    > [!div class="mx-imgBorder"]
    > ![Relationship analytics configuration page](media/si-admin-relationship-analytics-configuration-page.png "Relationship analytics configuration page")

4. Select **Enable Relationship analytics for your organization** to enable relationship analytics for your organization and then select **Save**.

    > [!div class="mx-imgBorder"]
    > ![Enable relationship assistant for organization](media/si-admin-relationship-analytics-enable-in-organization.png "Enable relationship assistant for organization")

    The Relationship analytics is enabled in your organization and you can configure the parameters as required.

5. Configure the parameters as described in the following table.

    |**Parameter**|**Description**|
    |-|-|
    |**Data Sources**|**CRM Activities:** If enabled, all historical data from [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] is ingested for computation in Relationship analytics.<br>**LinkedIn:** If enabled, the data from LinkedIn will be ingested for KPI and health computation. By default, the option is enabled when LinkedIn is installed in [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)].<br> **Note**: This option is not available if LinkedIn is not installed in [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)].<br>**Exchange Data:** If enabled, 30 days of data from Exchange is ingested for KPI and health computation. Exchange connector ingests three days of data per day until the last 30 days of data is complete.|
    |**Relationship Health Score**|Businesses place different emphasis on the type of communication used with customers. You can modify the importance of activities of different types as they contribute to the relationship health score.|
    |**Communications Frequency**|Businesses have varying sales cycles and different expected levels of communications with customers. A longer expected communications frequency reduces the expectation of more recent frequent communications in the health score. A shorter expected communications frequency increases the expectation of more recent frequent communications in the health score.|
    > [!div class="mx-imgBorder"]
    > ![Relationship analytics configuration settings page](media/si-admin-relationship-analytics-configuration-settings.png "Relationship analytics configuration settings page")

6. Select **Save**.

   Relationship analytics is ready to use in your organization.

Enable the **Dynamics 365 Sales Insights – Analytics** option in the admin center to collect valuable information regarding communications, such as emails and meetings for users in your organization from Exchange server. This data is used in analytics features for salespeople and sales managers. When you enable this, the **Exchange Data** option on the relationship analytics configuration page is automatically selected. 

To enable Dynamics 365 Sales Insights – Analytics, follow these steps: 

1. Go to the **Admin** center.

    > [!div class="mx-imgBorder"]
    > ![Admin center](media/sales-insights-addon-admincenter.png "Admin center")

2. Select **Settings** > **Services & add-ins** > **Dynamics 365 Sales Insights – Analytics**.

    > [!div class="mx-imgBorder"]
    > ![Select customer insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview.png "Select customer insights preview option")

3. Read the description and configure the Dynamics 365 Sales Insights – Analytics settings as **on** and select **Save**.

    > [!div class="mx-imgBorder"]
    > ![Enable and save customer insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview-settings.png "Enable and save customer insights preview option")

    Now you can connect to the Exchange server to collect data.

### See also

[View customer activity history](../sales/relationship-analytics.md)

[Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)

[Opt out of relationship analytics (GDPR)](optout-relationship-analytics-gdpr.md)

[GDPR for Sales Insights](embedded-intelligence-gdpr.md)

[View and export KPI data (GDPR)](view-export-KPI-data-gdpr.md)

[Retrieve insights data using msdyn_RetrieveTypeValuesFromDCI action](retrieve-insights-data-msdyn-RetrieveTypeValuesFromDCI.md)
