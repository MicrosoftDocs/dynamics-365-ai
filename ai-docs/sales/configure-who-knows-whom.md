---
title: "Configure who knows whom for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure who knows whom for Sales Insights"
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: c5e131e2-c4ba-4442-9580-dfc9badbc9ad
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Configure Who knows whom

The Who knows whom feature helps users to quickly identify colleagues within their organization who can introduce them to leads or contacts. To configure who knows whom, follow these steps:

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features) 

2.	Go to **Change area** and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3.  On the sitemap, select **Who knows whom** under **Connection insights**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Set up** from the **Who knows whom** section to go to configuration page.

    The configuration page opens.

    > [!div class="mx-imgBorder"]
    > ![Who knows whom configuration page](media/si-admin-who-know-whom-configuration-page.png "Who knows whom configuration page")

4. On the **Who knows whom** section, select **Turn on Who Knows Whom for your organization**.

    > [!div class="mx-imgBorder"]
    > ![Enable who knows whom](media/si-admin-who-knows-whom-enable.png "Enable who knows whom")
        
5. Optionally, you can select an email template according to your organizational requirements. By default, an out-of-the-box email template will be selected.

6. Select **Save**.

   The Who knows whom feature is configured and ready to use in your organization.

After you enable the Who knows whom feature in your organization, verify that the connection graph is enabled in the admin center. This allows [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] to collect the communication and collaboration details of users from Exchange server.

> [!NOTE]
> Contact your Office 365 administrator to enable the Dynamics 365 Sales Insights connection graph if you don't have sufficient privileges to enable. 
 
To configure the Dynamics 365 Sales Insights connection graph, follow these steps:

1. Go to the **Admin** center.

    > [!div class="mx-imgBorder"]
    > ![Admin center](media/sales-insights-addon-admincenter.png "Admin center")

2. Select **Settings** > **Services & add-ins** > **Dynamics 365 Sales Insights – Connection Graph**.

    > [!div class="mx-imgBorder"]
    > ![Select connection graph option](media/sales-insights-addon-admincenter-connection-graph-option.png "Select connection graph option")

3. Read the description and configure the Dynamics 365 Sales Insights – Connection Graph settings as **on**.

    > [!div class="mx-imgBorder"]
    > ![Enable and save connection graph](media/sales-insights-addon-admincenter-connection-graph-enable.png "Enable and save connection graph")

4. (Optional) If you don't want to collect information on a group of users in your organization, add the group ID in the text box. 

    > [!div class="mx-imgBorder"]
    > ![Enable and save connection graph](media/sales-insights-addon-admincenter-connection-graph-exclude-group.png "Enable and save connection graph")

5. Select **Save**.


### See also

[Get introduced to lead](../sales/who-knows-whom.md)

[Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)