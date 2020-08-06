---
title: "Configure email engagement for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure email engagement for Sales Insights"
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 04db6801-020a-4a99-9ad3-907422524b6f
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Configure email engagement

Email engagement helps the user in your organization to receive alerts and reminders that help build customer relationships.

> [!NOTE]
> To benefit from the complete experience of email engagement, turn on the email engagement insight cards - [Email opened](action-cards-reference.md#EmailOpened) and [Email reminder](action-cards-reference.md#EmailReminder).

> [!IMPORTANT]
> By enabling this feature, you consent to share data about your customers' email activity with other Microsoft services. Data imported from external systems into Dynamics 365 Sales Insights are subject to our privacy statement.

## Prerequisites

Verify the following prerequisites before enabling email engagement for your organization:

- To configure, enable standard Sales Insights features. To learn more, see [Enable and configure standard Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-standard-sales-insights-features).

- To use followed email attachments:

    - [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] must be available to your Dynamics 365 Sales server. To learn more, see [Enable OneDrive for Business](/dynamics365/customer-engagement/admin/enable-onedrive-for-business).  

    - Enable document management for email in Dynamics 365 Sales. To learn more, see [Enable SharePoint document management for specific entities](/dynamics365/customer-engagement/admin/enable-sharepoint-document-management-specific-entities).  

    - Enable SharePoint to be shared externally to anonymous (unauthenticated) users to allow external email recipients to access file attachments. To learn more, see [External sharing overview](https://docs.microsoft.com/sharepoint/external-sharing-overview).

- To enable delivery-time recommendations based on recipients' time zones, you must enable [!INCLUDE[pn_bing_maps](../includes/pn-bing-maps.md)] in Dynamics 365 Sales. To learn more, see [System Settings dialog box - General tab](/dynamics365/customer-engagement/admin/system-settings-dialog-box-general-tab).

## Enable email engagement

1.	Sign in to **Dynamics 365 Sales** and go to **Sales Hub** app.

2.	Go to **Change area** at the bottom-left of the page and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3. On the **Sales Insights settings** page, select **Grant Permissions** from the **Email engagement (standard)** section.

    > [!div class="mx-imgBorder"]
    > ![Email engagement grant permissions](media/si-admin-email-engagement-grant-permissions.png "Email engagement grant permissions") <br>

    A confirmation message is displayed in a tab. Close the tab and proceed to set up email engagement.

    > [!NOTE]
    > If you have already grant permissions, this step will be skipped. You don't have to grant permissions to email engagement again.<br>

4. On the **Email engagement** section, select **Set up** and then select the toggle to enable. 

    > [!div class="mx-imgBorder"]
    > ![Enable Email engagement](media/si-admin-email-engagement-enable.png "Enable Email engagement") <br>

    Email engagement is enabled and ready to use in your organization. 

### See also

[Introduction to administer Sales Insights](../sales/intro-admin-guide-sales-insights.md)

[View message interactions with email engagement](email-engagement.md)