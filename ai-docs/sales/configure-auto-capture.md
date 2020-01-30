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

When you enable auto capture, you help salespeople in your organization by suggesting relevant customer activities in Microsoft Dynamics 365 Sales by capturing emails and meetings from Outlook.

Auto capture is available in two forms:
<!--note from editor: Edit to the first line below is suggested, just to help later when we're contrasting the two versions. I didn't call it "basic auto capture" everywhere, but I did change some references later in this topic to clarify which version we're talking about. (Lines 39, 45, 53, and 65.)-->
-	**Auto capture** (also called _basic auto capture_): This feature is available for free with Dynamics 365 Sales Insights for Dynamics 365 Sales. To learn more, see [How to enable auto capture](#how-to-enable-auto-capture).

-	**Premium auto capture**: Premium auto capture is available as a preview <!--note from editor: This is still a preview feature? We need to add a public preview disclaimer in that case, yes?-->with Dynamics 365 Sales Insights for Dynamics 365 Sales. To learn more, see [How to enable and configure premium auto capture](#how-to-enable-and-configure-premium-auto-capture).

> [!IMPORTANT]
> By enabling this feature, you consent to share data about your customers' email activity with an external system. Data imported from external systems into Sales Insights are subject to the Microsoft Privacy Statement.<!--note from editor: Is this what you mean by "our privacy statement"? If so, should we link to it? https://privacy.microsoft.com/en-us/privacystatement If not, should we link to the relevant privacy statement? Should I ask Renee, or do you know what's the right thing to do here?-->

## Things you must know

Before you configure auto capture for Dynamics 365 Sales in your organization, note the following:

-	You can enable both basic and premium auto capture for your organization.

-	To enable both versions of auto capture, you select a group of security roles to use premium auto capture and you select other security roles to use auto capture.<!--note from editor: Edit suggested, maybe inaccurate. The original was a bit ambiguous: "...and other security roles will have auto capture." I assume that if a security role isn't defined for one type of auto capture or another, it won't be able to use auto capture at all? If that's not the case, please excuse and maybe explicitly say that any roles not assigned to use premium auto capture will default to basic.-->

-	When premium auto capture is enabled for your entire organization, basic auto capture is disabled.

## How to enable basic auto capture

Enable basic auto capture by following these steps:

1.	[Review prerequisites for auto capture](#prerequisites-for-auto-capture).

2.	[Enable auto capture](#enable-auto-capture).

### Prerequisites for basic auto capture

Before you enable auto capture, perform the following tasks: 

-	Enable Sales Insights. To learn more, see [Enable and configure free Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-free-sales-insights-features).

-	Use Microsoft Exchange Online as your email server.<!--note from editor: Should we specify Exchange as the server and Outlook as the mail client? We sometimes refer to Exchange data and Exchange account, and sometimes it's Outlook data. Should it be consistent?-->

-	Approve the email addresses of users to allow queries against their Exchange data (this requires tenant-level admin privileges). To learn more, see [Approve email](/dynamics365/customer-engagement/admin/connect-exchange-online#approve-email).

-	Set up server-side synchronization. To learn more, see [Set up server-side synchronization of email, appointments, contacts, and tasks](/dynamics365/customer-engagement/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks).

### Enable basic auto capture

1.	Sign in to the Dynamics 365 Sales Hub app, and go to **Change area** > **Sales Insights settings**.

2.	On the site map under **Productivity intelligence**, select **Auto capture**. 

3.	Turn on the **Enable basic auto capture** toggle.<!--note from editor: I think it would be better if the toggle were turned on in this image. Also, there should be a space in "365to". -->

   > [!div class="mx-imgBorder"]
   > ![Enable or disable auto capture](media/si-admin-auto-capture-enable-disable.png "Enable or disable auto capture")

## How to enable and configure premium auto capture
<!--note from editor: Please check this edit. I got a little lost here; this edit is my attempt to make it clear what you get extra with premium auto capture.-->
In addition to getting suggestions for customer-related activities through capturing emails and meetings, premium auto capture gets suggestions by capturing contacts through a salesperson's communications.

To enable and configure premium auto capture, follow these steps:

1.	[Review prerequisites for premium auto capture ](#prerequisites-for-premium-auto-capture).

2.	[Enable and configure premium auto capture](#enable-and-configure-premium-auto-capture).

### Prerequisites for premium auto capture

Before you enable premium auto capture, perform the following tasks:

-	Enable Sales Insights. To learn more, see [Enable and configure free Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-free-sales-insights-features).

-	Use Microsoft Exchange Online as your email server.<!--note from editor: As above. Should we specify Outlook as the client?-->

-	(Optional) Approve the email addresses of users to allow queries against Exchange (this requires tenant-level admin privileges) and set up server-side synchronization. If you don't configure these options, users will be required to provide consent to access their Outlook data. To learn more, see [Approve email](/dynamics365/customer-engagement/admin/connect-exchange-online#approve-email) and [Set up server-side synchronization of email, appointments, contacts, and tasks](/dynamics365/customer-engagement/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks).

### Enable and configure premium auto capture

1.	Sign in to the Dynamics 365 Sales Hub app, and go to **Change area** > **Sales Insights settings**.

2.	On the site map under **Productivity intelligence**, select **Auto capture**.

3.	On the settings page, in the **Premium auto capture (preview)** section, turn on the **Enable preview version** toggle<!--note from editor: The image shows the toggle label as "Preview version enabled."-->.

    > [!div class="mx-imgBorder"]
    > ![Enable or disable premium auto capture](media/si-admin-auto-capture-enable-premium.png "Enable or disable premium auto capture")
    
4.	Select one of the following options: 

    -	**All security roles**: Select this option to enable the feature for the entire organization.

    -	**Specific security roles**: Select this option to enable this feature for specific security roles, and then choose the security roles. In the example in the following image, we're adding the security roles **Sales Manager**, **Salesperson**, and **Marketing Manager**.<!--note from editor: The following image also shows the toggle as "Preview version enabled."-->

        > [!div class="mx-imgBorder"]
        > ![Add security roles](media/si-admin-auto-capture-premium-add-security-roles.png "Add security roles")

5.	Select the communication channels in which you want to capture customer-related activities. You can choose **Email**, **Calendar**, and **Contacts**.

6.	Save the settings.

Premium auto capture is now enabled for your organization. 

> [!NOTE]
> For more information about auto capture and how it can help your users, see [Capture customer-related activities with auto capture](auto-capture.md).

### See also

[Introduction to administering Sales Insights](intro-admin-guide-sales-insights.md)
