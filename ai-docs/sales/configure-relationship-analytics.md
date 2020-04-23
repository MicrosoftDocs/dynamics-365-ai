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

Relationship analytics provides graphical representation of KPIs and activity histories for any contact, opportunity, lead, or account to the users. 

To configure Relationship analytics, follow these steps:

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features) 

2. Go to **Change area** and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3. On the site map, select **Relationship analytics** under **Connection insights**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Manage** from the **Relationship analytics** section to go to configuration page.

    The configuration page opens.

4. Select the toggle to enable Relationship analytics for your organization.

    > [!div class="mx-imgBorder"]
    > ![Enable the relationship assistant for your organization](media/si-admin-relationship-analytics-enable-in-organization.png "Enable the relationship assistant for organization")

    Relationship analytics is enabled in your organization, and you can configure the parameters as required.

<a name="configure-similar-opportunities-preview"></a>

5. (Optional) To enable the preview to view similar opportunities, under **Similar opportunities** on the **Relationship analytics** tab for opportunities, turn on the **Preview enabled** toggle.

    By enabling this option, users in your organization can see an improved Relationship analytics tab for opportunities. The tab displays customer interaction KPIs along with suggestions calculated from similar won opportunities through AI-driven models.

    >[!NOTE]
    >- The preview feature is available only for the Opportunity entity.
    >- You must have at least 30 won and 30 lost opportunities to compare with existing opportunities.
    >- To understand how users use this feature, see [View similar opportunities](relationship-analytics.md#relationship-analytics-with-similar-opportunities).

    > [!div class="mx-imgBorder"]
    > ![Enable preview to view similar opportunities](media/relationship-analytics-enable-preview-similar-opportunities.png "Enable preview to view similar opportunities")

6. To show the relationship health score in opportunities, views, and charts, set the toggle to **On**.

    >[!NOTE]
    >You can disable the option if you don't wish to display the score in opportunities, views, and charts. However, disabling the option does not affect the process of gathering the relevant health data.

    > [!div class="mx-imgBorder"]
    > ![Enable relationship health for organization](media/relationship-analytics-relationship-health-enable.png "Enable relationship health for organization")

7. Adjust the importance of activities of different types as they contribute to the relationship health score.

    Businesses place different emphasis on the type of communication used with customers.The activities includes, Emails, Meetings, Phone calls, and Tasks. 
    
    > [!div class="mx-imgBorder"]
    > ![Adjust activity influence for relationship health](media/relationship-analytics-relationship-health-adjust-activity.png "Adjust activity influence for relationship health")

8. Choose **Communication Frequency**. 

    Businesses have varying sales cycles and different expected levels of communications with customers. A longer expected communications frequency reduces the expectation of more recent frequent communications in the health score. A shorter expected communications frequency increases the expectation of more recent frequent communications in the health score.

    > [!div class="mx-imgBorder"]
    > ![Choose communication frequency](media/relationship-analytics-communication-frequency.png  "Choose communication frequency")

9. Select **Save**.

   Relationship analytics is ready to use in your organization.

Enable the **Dynamics 365 Sales Insights – Analytics** option in the admin center to collect valuable information regarding communications&mdash;such as emails and meetings&mdash;for users in your organization from Exchange server. This data is used in analytics features for salespeople and sales managers. When you enable this, the **Exchange Data** option on the Relationship analytics configuration page is automatically selected. 

To enable Dynamics 365 Sales Insights – Analytics, follow these steps: 

1. Go to the **Admin** center.

    > [!div class="mx-imgBorder"]
    > ![Admin center](media/sales-insights-addon-admincenter.png "Admin center")

2. Select **Settings** > **Settings** > **Dynamics 365 Sales Insights – Analytics**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview.png "Select Sales Insights preview option")

3. Read the description carefully, select the **Allow org data to be used by ‎Dynamics 365 Sales Insights - Analytics**‎ option, and then select **Save changes**.

    > [!div class="mx-imgBorder"]
    > ![Enable and save Sales Insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview-settings.png "Enable and save Sales Insights preview option")

    Now you can connect to the Exchange server to collect data.

### See also

[View customer activity history](../sales/relationship-analytics.md)  
[Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)  
[Opt out of relationship analytics (GDPR)](optout-relationship-analytics-gdpr.md)  
[GDPR for Sales Insights](embedded-intelligence-gdpr.md)  
[View and export KPI data (GDPR)](view-export-KPI-data-gdpr.md)  
[Retrieve insights data using msdyn_RetrieveTypeValuesFromDCI action](retrieve-insights-data-msdyn-RetrieveTypeValuesFromDCI.md)
