---
title: "Configure auto capture for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure auto capture for Sales Insights"
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: d4d130c5-3494-4677-9093-0a0e0124d953
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Enable and configure auto capture

Auto capture helps sales personnel in your organization to add relevant customer activities to Dynamics 365 Sales by capturing emails and meetings from Outlook.
Auto capture is available in two forms:

-	**Auto capture**: This feature is available for free with Sales Insights on Dynamics 365 Sales. To learn more, see [How to enable Auto capture](#how-to-enable-auto-capture).

-	**Premium auto capture**: Premium auto capture is available as a preview with Sales Insights on Dynamics 365 Sales. To learn more, see [How to enable and configure premium auto capture](#how-to-enable-and-configure-premium-auto-capture).

> [!IMPORTANT]
> By enabling this feature, you consent to share data about your customers' email activity with an external system. Data imported from external systems into Dynamics 365 Sales Insights are subject to our privacy statement.

## Things you must know

Before you configure Auto capture for Dynamics 365 Sales in your organization, note the following:

-	You can enable both auto capture and premium auto capture for your organization.

-	To enable both versions of auto capture, you can select a group of security roles to use premium auto capture and other security roles will have auto capture.

-	When premium auto capture is enabled for your entire organization, auto capture is disabled.

## How to enable auto capture

To help sales personnel in your organization to track emails and meetings with their customers to Dynamics 365 Sales, enable auto capture.

To enable auto capture, follow these steps:

1.	[Review prerequisites for auto capture](#prerequisites-for-auto-capture)

2.	[Enable auto capture](#enable-auto-capture)

### Prerequisites for auto capture

Before you enable auto capture, perform the following tasks: 

-	Enable Sales Insights. To learn more, see [Enable and configure free Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-free-sales-insights-features).

-	Use Microsoft Exchange Online as your email server.

-	Approve email address of users to allow queries against Exchange (requires tenant-level admin privileges). To learn more, see [Approve email](/dynamics365/customer-engagement/admin/connect-exchange-online#approve-email).

-	Set up server-side synchronization. To learn more, see [Set up server-side synchronization of email, appointments, contacts, and tasks](/dynamics365/customer-engagement/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks).

### Enable auto capture

1.	Sign in to Dynamics 365 Sales Hub app, and go to **Change area** > **Sales Insights settings**.

2.	On the sitemap, select **Auto capture** under **Productivity intelligence**. 

3.	Select the toggle **Enable basic auto capture**. Auto capture is enabled for your organization.

   > [!div class="mx-imgBorder"]
   > ![Enable or disable Auto capture](media/si-admin-auto-capture-enable-disable.png "Enable or disable Auto capture")

## How to enable and configure premium auto capture

Premium auto capture introduces new experiences to capture customer-related activities by getting suggestions based on sales personnel’s Outlook data and get suggestions to create contacts based on the captured activities.

To enable and configure premium auto capture, follow these steps:

1.	[Review prerequisites for premium auto capture ](#prerequisites-for-premium-auto-capture)

2.	[Enable and configure premium auto capture](#enable-and-configure-premium-auto-capture)

### Prerequisites for premium auto capture

Before you enable premium auto capture, perform the following tasks:

-	Enable Sales Insights. To learn more, see [Enable and configure free Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-free-sales-insights-features).

-	Use Microsoft Exchange Online as your email server.

-	(Optional) Approve email address of users to allow queries against Exchange (requires tenant-level admin privileges) and Set up server-side synchronization. If you do not configure these options, users will be required to provide consent to access their Outlook. To learn more, see [Approve email](/dynamics365/customer-engagement/admin/connect-exchange-online#approve-email) and [Set up server-side synchronization of email, appointments, contacts, and tasks](/dynamics365/customer-engagement/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks).

### Enable and configure premium auto capture

1.	Sign in to Dynamics 365 Sales Hub app, and go to **Change area** > **Sales Insights settings**.

2.	On the sitemap, select **Auto capture** under **Productivity intelligence**.

3.	On the settings page, under the **Premium auto capture (preview)** section, set the toggle to **Enable preview version**. 
    
    The preview version is enabled.

   > [!div class="mx-imgBorder"]
   > ![Enable or disable Premium auto capture](media/si-admin-auto-capture-enable-premium.png "Enable or disable Premium auto capture")
    
4.	Select one of the following options: 

    -	**All security roles**: Select this option to enable the feature for the entire organization.

    -	**Specific security roles**: Select this option to enable this feature for specific security roles and choose the security roles. In the following example, we are adding security roles **Sales Manager**, **Salesperson**, and **Marketing Manager**.

       > [!div class="mx-imgBorder"]
       > ![Add security roles](media/si-admin-auto-capture-premium-add-security-roles.png "Add security roles")

5.	Choose the communication channels to capture customer related activities. You can choose **Email**, **Calendar**, and **Contacts**.

6.	Save the settings.

    Premium auto capture is enabled for your organization. 

> [!NOTE]
> For more information about Auto capture and how it can help your users, see [Auto capture](auto-capture.md)

### See also

[Introduction to administer Sales Insights](intro-admin-guide-sales-insights.md)

[Display related emails with auto capture](auto-capture.md)
