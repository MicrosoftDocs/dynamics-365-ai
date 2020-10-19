---
title: "First-run set up experience for conversation intelligence | MicrosoftDocs"
description: "First-run set up experience for conversation intelligence"
ms.date: 04/09/2020
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 3e099e3a-f6cb-42cf-b84e-9f8b0c6ee9db
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# First-run set up experience of conversation intelligence

you can configure the conversation intelligence through [conversation intelligence application](#configure-in-conversation-intelligence-application) or through [Sales Hub app](#configure-in-sales-hub-app). 
When you sign in to conversation intelligence, the application will be available for you to use and explore the various features through the provided demo data.
After you sign in, you can set up the application depending on the role that is assigned to you.

-	As an administrator, you can set up the complete application including connecting Dynamics 365 Sales environment, grant app permissions, connect call data, enable preview, and define tracked key words and competitors to use the features that the application offers.

-	As a sales manager or seller, you can access the application with demo data and administrator must configure the application to view the data relevant to you.

## Configure in conversation intelligence application

The following diagram illustrates the process of setting up application as an administrator:

> [!div class="mx-imgBorder"]
> ![Process of setting up conversation intelligence through different user roles](media/si-app-fre-admin-endusers.png "Process of setting up conversation intelligence through different user roles")

1.	Review the perquisites. To learn more, see [Prerequisites to setup conversation intelligence](prereq-sales-insights-app.md).

2.	Sign in to **Conversation intelligence** application as administrator.

    > [!div class="mx-imgBorder"]
    > ![Administrator conversation intelligence home page](media/si-app-admin-home-page-admin-signin.png "Administrator conversation intelligence home page")
 
3.	Select **Set up Conversation intelligence** and continue with the setup wizard. 

4.	On the **Connect your data** dialog box, select your Dynamics 365 Sales environment to connect with the application.

    > [!div class="mx-imgBorder"]
    > ![Select Dynamics 365 Sales environment](media/si-app-admin-connect-d365-organization.png "Select Dynamics 365 Sales environment")
  
    The application detects your environment.

5.	On the **Terms and conditions** dialog box, carefully read and select the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement) and [terms and conditions](https://www.microsoft.com/licensing/product-licensing/products). Select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/si-app-admin-accept-tandc.png "Accept terms and conditions")

    >[!NOTE]
    >Selecting the first check box, allows Microsoft to collect your organization's data to improve the quality of insights. This check box is optional.

    The application takes few minutes to connect your data with application and progress dialog box is displayed.
 
    > [!div class="mx-imgBorder"]
    > ![Environment connection progress](media/si-app-admin-connection-progress-d365-org.png "Environment connection progress")
  
6.	On the **Create an application user** dialog box, select **Grant permissions** to create application user to use the application.

    > [!div class="mx-imgBorder"]
    > ![Grant permissions to create application user](media/si-app-admin-grant-permission-create-app-user.png "Grant permissions to create application user")
 
    The permission is granted to use the application.

7.	On the **Connect your call data** dialog box, enter the **Storage connection string** and **Container name** and select **Connect**.
    
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
 
10.	Select **Finish** to complete the set-up of conversation intelligence for your organization.

    The status message will be displayed on the top of the page.

    > [!div class="mx-imgBorder"]
    > ![Set up progress message](media/si-app-admin-status-message-set-up.png "Set up progress message")
  
Now, your conversation intelligence is ready, and managers and sellers can use to view this data.


## Configure in Sales Hub app

Perform the following steps to configure conversation intelligence through the Sale Hub app:

1.	You must have an administrator or equivalent security role. To learn more, see [Assign a security role to a user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user).

2.	Sign in to Dynamics 365 Sales, and go to the **Sales Hub** app.

3.	Go to **Change area** in the lower-left corner of the page and select **Sales Insights settings**. 

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings")

4.	In the configuration page, under **Productivity**, select **Conversation intelligence**. 

    > [!div class="mx-imgBorder"]
    > ![Conversation intelligence configuration page](media/ci-admin-config-page.png "Conversation intelligence configuration page")

5.	Under the **Call recording storage** section, configure the storage-related options as described:

    - **Storage location**: Enter the **Storage connection string** and **Container name** to upload the call recordings for analysis. More information: [Configure conversation intelligence to connect call data](../sales/configure-conversation-intelligence-call-data.md).

    - **Retention policy**: Choose a retention time limit, the application retains the call recording data for the specified time limit and deletes when the time limit is reached. More information: [Retention Policy](data-retention-deletion-policy.md#retention-policy). 

    > [!div class="mx-imgBorder"]
    > ![Configuration call recording storage](media/ci-admin-connection-storage.png "Configuration call recording storage")

6.	Under the **Conversation tracking** section, add the keywords and competitors that you want to track on the call. You can update these keywords and trackers later when your organization requires a change. Also, you can add languages in which the sellers may use during their calls with customers. More information: [Configure keywords, competitors, and languages in Conversation content](../sales/configure-keywords-competitors.md).

    > [!div class="mx-imgBorder"]
    > ![Configuration conversation trackers](media/ci-admin-conversation-trackers.png "Configuration conversation trackers")

    >[!NOTE]
    >-	Storage and conversation tracking are the only required field for the first-time onboarding to Conversation Intelligence. Now you can already publish the settings if you want. Go to step 11. 
    >-	Sales managers can configure the conversation trackers specific to their team.

7.	Under the **Sales team management** section, configure the top sellers and hierarchy options as described:

    - **Call data visibility**: Select the levels of hierarchy for which sales managers can view in conversation intelligence data.

    - **Team members and top performers**: You can view the names of your team members who's calls are being analyzed in conversation intelligence, select which of them are your top performers, and delete their data if necessary.

        You can choose the top performers manually or let the application choose automatically. Select an option as required:

        - **Manually select top performers**: Allows you to manually choose the top performers from the list of sellers. Under the **Top performer** column, select the star icon corresponding to a seller. The seller is added to the top performers list on which the seller's data is compared against other sellers. 

        - **Enable automatic identification of top performers**: Allows the application to automatically select the top performers based on the amount of leads they qualified or opportunities they won. When you select to automatically select to performers, the drop-down list is enabled to choose **by won opportunities** or **by lead qualification**. Choose an option appropriate. 

    > [!div class="mx-imgBorder"]
    > ![Choose and confiogure sales team](media/ci-admin-choose-sales-team.png "Choose and confiogure sales team")              

    You can skip configuring this section and add them later when required. To learn more, see [Configure sales team information in Sales Hub app](../sales/configure-view-your-team-page.md#configure-sales-team-information-in-sales-hub-app).

8.	Under the **License usage** section, you can view the information on the total call recording processing hours left and used. This is view only and can’t be changed.

    > [!div class="mx-imgBorder"]
    > ![View license usage information](media/ci-admin-license-usage.png "View license usage information")
 
9.	Under the **Privacy** section, selecting the check box to allow Microsoft to improve the quality of insights through read-only access to your organization’s data in conversation intelligence. This is optional. 

    > [!div class="mx-imgBorder"]
    > ![Enable privacy](media/ci-admin-enable-privacy.png "Enable privacy")
 
10.	Under the **Coming soon** section, select the **Access new features before they’re released to all our customers** option to turn the coming soon feature.
    
    If you don’t want to enable the preview feature for your organization, skip this step to proceed. You can always enable the preview features later. To learn more, see [Enable coming soon features](../sales/enable-preview-features-sales-insights-app.md).

    > [!div class="mx-imgBorder"]
    > ![Enable coming soon features](media/ci-admin-coming-soon-features.png "Enable coming soon features")

11.	Select **Save + publish**.
    
    A message is displayed to accept the terms and conditions. Read the terms and conditions, and privacy statement carefully. Select **Agree and continue**.
    
    > [!div class="mx-imgBorder"]
    > ![Agree terms and conditions to publish the configurations](media/ci-admin-agree-terms-conditions-to-publish.png "Agree terms and conditions to publish the configurations")
    
    Conversation intelligence is configured and ready for use in your organization.

### See also

[Introduction to administer conversation intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)

[Prerequisites to use conversation intelligence](prereq-sales-insights-app.md)