---
title: "First-run setup experience for call insights | MicrosoftDocs"
description: "First-run setup experience for call insights"
ms.date: 04/20/2020
ms.service: 
 - dynamics-365-ai
ms.custom: 
ms.topic: article
author: lalexms
ms.author: laalexan
manager: shujoshi 

---

# First-run setup experience for call insights

When you sign in to Customer Service Insights for the first time, you can use and explore the various call insights features through the provided demo data.

Depending on your role:

-	As an administrator, you can set up the complete call insights features, including connecting your Dynamics 365 Customer Service environment, granting app permissions, connecting call data, enabling preview, and defining tracked key words and to use. 

-	As a supervisor or agent, you can access the application with demo data. Ask your administrator to configure call insights so you can view the data relevant to you.

## Administrator setting up application

1.	Review the prerequisites. To learn more, see [Prerequisites to configure call insights](ci-admin-prereqs-app.md).

2.	Sign in to the Dynamics 365 Customer Service Insights application.

3.	Select **My workspaces** > **Call insights (preview)**.

    > [!div class="mx-imgBorder"]
    > ![Select call insights from My workspaces](media/ci-workspace-view.png "Access the call insights feature from the My workspaces menu")

4.	If you are viewing call insights for the first time, you will see a banner-type message at the top that is prefaced with **DEMO APP: Explore the app with sample data.** To set up call insights, select the **set up call insights** link in the banner message.

    > [!div class="mx-imgBorder"]
    > ![Select set up call insights link](media/ci-first-signin.png "Select the set up call insights link")

5.	Select your Dynamics 365 environment to connect to. This helps to compute and consolidate the necessary insights about your team.

    > [!div class="mx-imgBorder"]
    > ![Select Dynamics 365 environment](media/ci-select-environment.png  "Select your Dynamics 365 environment")

6.	In the **Terms and conditions** dialog box, accept the terms and conditions and then select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/ci-app-tnc.png  "Accept terms and conditions")
 
    The application takes few minutes to connect your data with application and progress dialog box is displayed.
 
    > [!div class="mx-imgBorder"]
    > ![Environment connection progress](media/si-app-admin-connection-progress-d365-org.png "Environment connection progress")
  
7.	On the **Create an application user** dialog box, select **Grant permissions** to create application user to use the application.

    > [!div class="mx-imgBorder"]
    > ![Grant permissions to create application user](media/si-app-admin-grant-permission-create-app-user.png "Grant permissions to create application user")
 
    The permission is granted to use the application.

8.	On the **Connect your call data** dialog box, enter the **Storage connection string** and **Container name** and select **Connect**.
    
    To learn more on how to get these values, see [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md).

    > [!div class="mx-imgBorder"]
    > ![Enter values to connect call data](media/si-app-admin-connect-call-data.png "Enter values to connect call data")
 
8.	If you want to turn the coming soon feature, on the **Coming soon** dialog box, select the preview feature and then select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Turn on preview feature](media/si-app-admin-enable-preview-feature.png "Turn on preview feature")
 
    > [!NOTE]
    > If you don’t want to enable the preview feature for your organization, skip this step to proceed. You can always enable the preview features later. To learn more, see [Enable coming soon features](enable-preview-features-sales-insights-app.md).

9.	On the **Keyword and competitor tracking** dialog box, add the keywords and competitors that you want to track on the call. You can update these keywords and trackers later when your organization requires a change. To learn more, see [Configure keywords and competitors in Conversation content](configure-keywords-competitors.md).

    > [!NOTE]
    > You can also skip adding the keywords and competitors and add them later when required.

    > [!div class="mx-imgBorder"]
    > ![Add tracked keywords and competitors](media/si-app-admin-keywords-and-competitor-tracking.png "Add tracked keywords and competitors")
 
10.	Select **Finish** to complete the call insights configuration for your organization.

    The status message will be displayed on the top of the page.

    > [!div class="mx-imgBorder"]
    > ![Set up progress message](media/si-app-admin-status-message-set-up.png "Set up progress message")
  
Now, your call insights feature is ready, and supervisors and agents can use it to view the data.

### See also

[Introduction to administer Conversation Intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)

[Prerequisites to use call insights](ci-admin-prereqs.md)
