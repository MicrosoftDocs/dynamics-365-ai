---
title: "Overview of Customer Service Insights Call Intelligence | MicrosoftDocs"
description: "Improve agent coaching and customer experience with AI-driven insights readily available for Conversation Intelligence"
ms.date: 04/20/2020
ms.service: 
 - dynamics-365-ai
ms.custom: 
ms.topic: article
author: lalexms
ms.author: laalexan
manager: shujoshi 

---

# Improve agent coaching and customer experience with Conversation Intelligence

Conversation Intelligence uses analytics and data science to gather data from agents’ call recordings and Dynamics 365 Customer Service Insights. Conversation Intelligence analyzes the data to provide you with the information and insights to intelligently manage your team and proactively coach agents. To achieve this, Conversation Intelligence displays relevant key performance indicators (KPIs) and intelligent call data KPIs by team, agent, and call.

Conversation Intelligence is designed to help supervisors and agents in their day-to-day jobs, providing the tools they need to track their performance in calls with leads and customers.

**As a supervisor, you can:**

-	View and compare what’s happening in agent calls and get insights into best practices by learning more about the behaviors of your top agents. 

-	View your team’s performance, with insights, customer sentiment, and conversational style.

-	View and understand each individual agent’s conversation style, customer sentiment, insights, and call history. 

-	Listen to calls, read transcripts, see possible action items, and view business-critical insights.

-	Translate non-English call transcript to English.


**As an administrator, you can:**

-	Configure tracked keywords that your supervisors want to track for their teams’ calls with customers.

-	Configure how long you want to retain a team’s or individual agent’s data from your organization.

-	Manage environments and configure call data.

-	Monitor call and insight processing data.

-	Configure the levels of hierarchy for which supervisorss can view the call data.


The next sections describe:

- Recommendations for using Conversation Intelligence

- How to get Conversation Intelligence

- How to access Conversation Intelligence


## Recommendations to use Conversation Intelligence

Before you start using the application, we suggest you review the following requirements for effective use of Conversation Intelligence:

-	Verify that you have a subscription to Microsoft Dynamics 365 Customer Service Insights. To learn more, see [About licensing and license management](https://docs.microsoft.com/power-platform/admin/wp-license-management). 

-	As an administrator, verify that the proper hierarchy is defined for you, and that supervisors or individuals are added to it. 

## How to get Conversation Intelligence

Conversation Intelligence is a standalone application and you must sign in to the app to use it. To access the app, go to [customerserviceinsights.ai.dynamics.com](https://customerserviceinsights.ai.dynamics.com/).

## How to access Conversation Intelligence

As an administrator, you must configure the application so users (managers and sellers) can see the relevant organization and call data. To learn more, see [First-run setup experience](fre-setup-sales-insight-app.md).

As a user (supervisor or agent), when you sign in to the application for the first time, you might see the following:

- **Sample data**: This occurs if the administrator hasn't configured the application for you. The sample data helps you to explore the features and functionalities so you can shorten your learning curve.

- **Relevant organization and call data**: You’ll be able to view your organization’s data if the administrator has configured the application for you.

The following procedure explains how to access Conversation Intelligence for the first time:

1.	Sign in to the [Conversation Intelligence](https://customerserviceinsights.ai.dynamics.com/) application. The home page is displayed with demo data.

2.	Select **Set up Conversation Intelligence** to connect to your Dynamics 365 Customer Service Insights organization.

    > [!div class="mx-imgBorder"]
    > ![Conversation Intelligence application first sign-in](media/ci-app-first-signin.png "Conversation Intelligence application first sign-in")

3.	Select the Dynamics 365 Customer Service Insights organization to connect to. This helps to compute and consolidate the necessary insights about your team.

    > [!div class="mx-imgBorder"]
    > ![Select Dynamics 365 Customer Service Insights organization](media/ci-app-select-organization.png  "Select Dynamics 365 Customer Service Insights organization")

4.	In the **Terms and condition** dialog box, accept the terms and conditions and then select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/ci-app-tnc.png  "Accept terms and conditions")

	The application validates your credentials and gives you further instructions, depending on your role. If you have an administrator role assigned to you, you can proceed with configuring the application. To learn more, see [First-run setup experience](fre-setup-sales-insight-app.md).
    
    If you don't have the administrator role assigned to you, a status message is displayed on the top of the page, requesting that you contact your administrator to configure the application. You can continue using Conversation Intelligence (with the demo data to explore the features and functionalities) until the administrator configures the application.

### See also

[Administer Conversation Intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)

[View overall sales and seller insights](dynamics365-sales-insights-app-home-page.md)
