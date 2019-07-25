---
title: "Improve seller coaching and sales potential with Dynamics 365 Sales Insights application | MicrosoftDocs"
description: "Improve seller coaching and sales potential with AI-driven insights readily available for Dynamics 365 for Sales"
keywords: "conversation intelligence, Dynamics 365 Sales Insights, AI for sales, Sales AI, Sales Insights"
ms.date: 07/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
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

Applies to [!INCLUDE[pn-crm-online](../includes/pn-crm-online.md)] version 9.1.0.

The [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application uses analytics and data science to gather data from call recordings, [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)], and Microsoft Office. It then provides you with the information and insights to intelligently manage the sales team, proactively coach sellers, and quickly answer questions regarding the business. To achieve this, the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application provides you with information through key performance indicators (KPIs) for pipeline and deals, and intelligent call data KPIs through conversations intelligence.

This application is designed to help sales managers and sellers in their day-to-day job to keep track of their work. 

**As a sales manager, you can**

-	View and compare what’s happening in sales calls and insights on the behaviors of your top sellers<!--, and the sales pipeline for the timeline-->. To learn more, see [View team information](conversation-intelligence-team-overview.md)

-	View team’s insights, customer sentiment, and team’s conversational style<!--, and sales pipeline-->. To learn more, see [View team information](conversation-intelligence-team-overview.md).

-	View and understand individual seller’s conversation style<!--, sales pipeline-->, customer sentiment, insights, and call history. To learn more, see [View sales rep information](conversation-intelligence-seller-details.md).

-	View insights on the status of your current sales period such as the sum of actual revenue, total estimated revenues, total deals won, and the average revenue generated. To learn more, see [View overall sales and seller insights](dynamics365-sales-insights-app-home-page.md).

**As a seller, you can**

-	View your conversation insights, customer sentiment, conversations style, sales pipeline, and call history. To learn more,  see [View sales rep information](conversation-intelligence-seller-details.md).

**As a administrator, you can**

-	Configure tracker keywords and competitors that you want to track for your team’s calls with customers. To learn more, see [Configure keywords and competitors to track](configure-keywords-competitors.md).

    > [!NOTE]
    > Sales managers can also define tracker keywords and competitors. These trackers keywords and competitors apply only to their team.

-	Configure how long you want to retain or delete team’s or individual seller’s data from your organization. To learn more, see [Data retention and deletion through Privacy](data-retention-deletion-policy.md).

-	Manage environments and configure call data. To learn more, see [Connect to Dynamics 365 for Sales environment](connect-dynamics365-sales-environment.md) and [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md)

-	Enable preview for natural language Q&A. To learn more, see [Enable preview features](enable-preview-features-sales-insights-app.md).


The next sections describe:

- Recommendations for using the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application

- How to get the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application

- How to access the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application


## Recommendations to use Sales Insights application

Before you start using the application, we suggest you review the following requirements for effective use of the [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] app:

-	Verify that you have a subscription to Microsoft Dynamics 365 for Sales. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Purchase and assign Dynamics 365 for Customer Engagement apps licenses](/dynamics365/customer-engagement/admin/purchase-assign-online-licenses) 

<!-- - Verify that the fiscal year period is configured for your organization. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Work with fiscal year settings](/dynamics365/customer-engagement/admin/work-fiscal-year-settings)-->

- As a sales manager, verify that the proper manager hierarchy is defined for you, and that sellers or individuals are added to it. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Set up manager and position hierarchies](/dynamics365/customer-engagement/admin/hierarchy-security#set-up-manager-and-position-hierarchies)

<!-- - As a sales manager, verify that goals are defined for sellers or individuals in your hierarchy.[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create or edit a goal (Sales and Sales Hub)](/dynamics365/customer-engagement/sales-enterprise/create-edit-goal-sales)
    >[!NOTE]
    >While defining goals, ensure that **Goal Metric** parameter is configured as **Revenue**. -->

## How to get the Dynamics 365 Sales Insights application

The [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application is a standalone application and you must sign into the app to use it. To access the app, go to [sales.ai.dynamics.com](https://sales.ai.dynamics.com/).

## How to access the Dynamics 365 Sales Insights application

As an administrator, you must configure the application so users (managers and sellers) could see the relevant organization and call data. To learn more, see [First-run set up experience](fre-setup-sales-insight-app.md).

As a user (manager or seller), when you sign to the application for the first time, you might see the following:

- **Sample data**: If the administrator hasn't configured the application for you. The sample data helps you to explore the features and functionalities so you can enhance your learning curve.

- **Relevant organization and call data**: If the administrator has configured the application for you.

The following procedure explains how to access Sales Insights application for the first time:

1.	Signs into [Dynamics 365 Sales Insights](https://sales.ai.dynamics.com/) application, the home page is displayed with the demo data.

2.	Selects **Set up Sales Insights** to connect to Dynamics 365 for Sales organization.

    > [!div class="mx-imgBorder"]
    > ![Sales insights application first sign in](media/si-app-manager-first-signin.png "Sales insights application first sign in")

3.	Selects the Dynamics 365 for Sales organization to connect and this helps to compute and consolidate the necessary insights about your team.

    > [!div class="mx-imgBorder"]
    > ![select Dynamics 365 sales organization](media/si-app-select-organization.png  "select Dynamics 365 sales organization")

4.	On the **Terms and condition** dialog, accepts the terms and conditions, and selects **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/si-app-tnc.png  "Accept terms and conditions")

	The application validates your credentials and gives you further instructions depending on your role. If you have administrator role assigned to you, you can proceed with configuring the application. To learn more, see [First-run set up experience](fre-setup-sales-insight-app.md).
    
    If you don't have the administrator role assigned to you, a status message is displayed on the top of the page specifying you to contact your administrator to configure the application. However, you can continue with the demo data to explore the features and functionalities to enhance your learning curve until the administrator configures the application.
    
    > [!div class="mx-imgBorder"]
    > ![Application status message when manager signs in](media/si-app-admin-message-bar-manager.png  "Application status message when manager signs in")

## Privacy notice  

For specific privacy information about [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] capabilities for sales managers, see [Privacy notice](privacy-notice-manager.md).

### See also

- [Introduction to administer Sales Insights application](intro-admin-guide-sales-insights-app.md)

- [View overall sales and seller insights](dynamics365-sales-insights-app-home-page.md)