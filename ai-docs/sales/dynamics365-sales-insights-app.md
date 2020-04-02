---
title: "Improve seller coaching and sales potential with Dynamics 365 Sales Insights application | MicrosoftDocs"
description: "Improve seller coaching and sales potential with AI-driven insights readily available for Dynamics 365 Sales Insights"
ms.date: 07/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 17cac16d-2a37-4a19-9cfe-2d4355a6f044
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Improve seller coaching and sales potential with Dynamics 365 Sales Insights application

The [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application uses analytics and data science to gather data from call recordings, [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)], and Microsoft Office. It then provides you with the information and insights to intelligently manage the sales team, proactively coach sellers, and quickly answer questions regarding the business. To achieve this, the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application provides you with information through key performance indicators (KPIs) for pipeline and deals, and intelligent call data KPIs through conversations intelligence.

<div class=embeddedvideo><iframe src=https://go.microsoft.com/fwlink/?linkid=2099797 frameborder=0 allowfullscreen=></iframe></div>

This application is designed to help sales managers and sellers in their day-to-day job to keep track of their work. 

**As a sales manager, you can:**

-	Understand what customers are talking about to get strategic insights on trending tracked keywords, brands, and competitors that allow you to design sales strategies and training of your team. To learn more, see [View home page](dynamics365-sales-insights-app-home-page.md).

-	Understand if your opportunities and leads are losing momentum and be on top them to convert into deals. To learn more, see [Are my team’s deals on track?](dynamics365-sales-insights-app-home-page.md#are-my-teams-deals-on-track) 

-	View and compare what’s happening in sales calls and insights on the behaviors of your top sellers. To learn more, see [View team information](conversation-intelligence-team-overview.md).

-	View team’s insights, customer sentiment, and team’s conversational style. To learn more, see [View team information](conversation-intelligence-team-overview.md).

-	View and understand an individual seller’s conversation style, customer sentiment, insights, and call history. To learn more, see [View sales rep information](conversation-intelligence-seller-details.md).

-	View insights on the status of your current sales period such as the sum of actual revenue, total estimated revenues, total deals won, and the average revenue generated. To learn more, see [View overall sales and seller insights](dynamics365-sales-insights-app-home-page.md).

-	Listen to conversation and read transcript to get action items, signals, and business-critical insights. To learn more, see [call summary page]().  

**As a seller, you can:**

-	View your conversation insights, customer sentiment, conversations style, sales pipeline, and call history. To learn more,  see [View sales rep information](conversation-intelligence-seller-details.md).

-	Listen to conversation and read transcript to get action items, signals, and business-critical insights. To learn more, see [call summary page](). 

**As an administrator, you can:**

-	Configure tracker keywords and competitors that you want to track for your team’s calls with customers. To learn more, see [Configure keywords and competitors to track](configure-keywords-competitors.md).

    > [!NOTE]
    > Sales managers can also define tracker keywords and competitors. These trackers keywords and competitors apply only to their team.

-	Configure how long you want to retain or delete team’s or individual seller’s data from your organization. To learn more, see [Data retention and deletion through Privacy](data-retention-deletion-policy.md).

-	Manage environments and configure call data. To learn more, see [Connect to Dynamics 365 sales environment](connect-dynamics365-sales-environment.md) and [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md).

-	




The next sections describe:

- Recommendations for using the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application

- How to get the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application

- How to access the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application


## Recommendations to use Sales Insights application

Before you start using the application, we suggest you review the following requirements for effective use of the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] app:

-	Verify that you have a subscription to Microsoft Dynamics 365 Sales. To learn more, see [About licensing and license management](https://docs.microsoft.com/power-platform/admin/wp-license-management). 

- As a sales manager, verify that the proper manager hierarchy is defined for you, and that sellers or individuals are added to it. To learn more, see [Set up manager and position hierarchies](/dynamics365/customer-engagement/admin/hierarchy-security#set-up-manager-and-position-hierarchies).

## How to get the Dynamics 365 Sales Insights application

The [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application is a standalone application and you must sign in to the app to use it. To access the app, go to [sales.ai.dynamics.com](https://sales.ai.dynamics.com/).

## How to access the Dynamics 365 Sales Insights application

As an administrator, you must configure the application so users (managers and sellers) can see the relevant organization and call data. To learn more, see [First-run setup experience](fre-setup-sales-insight-app.md).

As a user (manager or seller), when you sign in to the application for the first time, you might see the following:

- **Sample data**: If the administrator hasn't configured the application for you. The sample data helps you to explore the features and functionalities so you can enhance your learning curve.

- **Relevant organization and call data**: If the administrator has configured the application for you.

The following procedure explains how to access the Sales Insights application for the first time:

1.	Sign in to the [Dynamics 365 Sales Insights](https://sales.ai.dynamics.com/) application. The home page is displayed with the demo data.

2.	Select **Set up Sales Insights** to connect to the Dynamics 365 Sales organization.

    > [!div class="mx-imgBorder"]
    > ![Sales insights application first sign-in](media/si-app-manager-first-signin.png "Sales insights application first sign-in")

3.	Select the Dynamics 365 Sales organization to connect to. This helps to compute and consolidate the necessary insights about your team.

    > [!div class="mx-imgBorder"]
    > ![Select Dynamics 365 sales organization](media/si-app-select-organization.png  "Select Dynamics 365 sales organization")

4.	On the **Terms and condition** dialog box, accept the terms and conditions and then select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/si-app-tnc.png  "Accept terms and conditions")

	The application validates your credentials and gives you further instructions depending on your role. If you have an administrator role assigned to you, you can proceed with configuring the application. To learn more, see [First-run setup experience](fre-setup-sales-insight-app.md).
    
    If you don't have the administrator role assigned to you, a status message is displayed on the top of the page specifying you to contact your administrator to configure the application. However, you can continue with the demo data to explore the features and functionalities to enhance your learning curve until the administrator configures the application.
    
    > [!div class="mx-imgBorder"]
    > ![Application status message when manager signs in](media/si-app-admin-message-bar-manager.png  "Application status message when manager signs in")

### See also

[Administer Sales Insights application](intro-admin-guide-sales-insights.md#administer-sales-insights-application)

[View overall sales and seller insights](dynamics365-sales-insights-app-home-page.md)
