---
title: "First-run setup experience for conversation intelligence | MicrosoftDocs"
description: "First-run setup experience for conversation intelligence"
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

# First-run setup experience for conversation intelligence
<!--note from editor: The title, description, and H1 all need to be unique.-->
You can configure conversation intelligence through the [conversation intelligence application](#configure-the-conversation-intelligence-application) or through the [Sales Hub app](#configure-in-the-sales-hub-app). 
When you sign in to conversation intelligence, the application will be available for you to use and explore the various features through the demo data provided.
After you sign in, you can set up the application depending on the role that's assigned to you.

- As an administrator, you can set up the complete application&mdash;including connecting to a Dynamics 365 Sales environment&mdash;grant app permissions, connect call data, enable the preview, and define tracked key words and competitors to use the features that the application offers.

- As a sales manager or seller, you can access the application by using demo data. An administrator must configure the application so you can view the data that's relevant to you.

## Configure the conversation intelligence application

The following image illustrates the process of setting up the application as an administrator.<!--note from editor: You'll want to use the new ::image:: extension so you can write longer, more detailed alt text for this image. Imagine that you either can't see the image or you've turned off graphics (reading on a mobile phone, perhaps), and think of how you'd describe what this image is showing. -->

> [!div class="mx-imgBorder"]
> ![Process of setting up conversation intelligence through different user roles](media/si-app-fre-admin-endusers.png "Process of setting up conversation intelligence through different user roles")

1.	Review the prerequisites. More information: [Prerequisites to setup conversation intelligence](prereq-sales-insights-app.md)

2.	Sign in to the conversation intelligence application as an administrator.

    > [!div class="mx-imgBorder"]
    > ![Administrator conversation intelligence home page](media/si-app-admin-home-page-admin-signin.png "Administrator conversation intelligence home page")
 
3.	Select **Set up Conversation intelligence**. 

4.	In the **Connect your data** dialog box, select your Dynamics 365 Sales environment to connect with the application.

    > [!div class="mx-imgBorder"]
    > ![Select Dynamics 365 Sales environment](media/si-app-admin-connect-d365-organization.png "Select Dynamics 365 Sales environment")
  
    The application detects your environment.

5.	In the **Terms and conditions** dialog box, carefully read the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement), and read and select the check box for the [terms and conditions](https://www.microsoft.com/licensing/product-licensing/products). Select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/si-app-admin-accept-tandc.png "Accept terms and conditions")

    >[!NOTE]
    >Selecting the first check box allows Microsoft to collect your organization's data to improve the quality of insights. This check box is optional.

    The application takes few minutes to connect your data with application. A progress dialog box is displayed.
 
    > [!div class="mx-imgBorder"]
    > ![Environment connection progress](media/si-app-admin-connection-progress-d365-org.png "Environment connection progress")
  
6.	In the **Create an application user** dialog box, select **Grant permissions** to create an application user to use the application.

    > [!div class="mx-imgBorder"]
    > ![Grant permissions to create application user](media/si-app-admin-grant-permission-create-app-user.png "Grant permissions to create application user")
 
    The permission is granted to use the application.

7.	In the **Connect your call data** dialog box, enter the **Storage connection string** and **Container name**, and then select **Connect**. More information: [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md)

    > [!div class="mx-imgBorder"]
    > ![Enter values to connect call data](media/si-app-admin-connect-call-data.png "Enter values to connect call data")
 
8.	If you want to turn on access to preview features<!--note from editor: Edit okay?-->, in the **Coming soon** dialog box, select the check box and then select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Turn on preview features](media/si-app-admin-enable-preview-feature.png "Turn on preview features")
 
    > [!NOTE]
    > If you don't want to enable the preview feature for your organization, skip this step. You can always enable preview features later. More information: [Enable coming soon features](enable-preview-features-sales-insights-app.md)

9.	In the **Keyword and competitor tracking** dialog box, add the keywords and competitors that you want to track on the call. You can update these keywords and trackers later if your organization's requirements change<!--note from editor: Suggested.-->. More information: [Configure keywords and competitors in Conversation content](configure-keywords-competitors.md)

    > [!NOTE]
    > You can also skip adding the keywords and competitors at this point. You can always add them later.

    > [!div class="mx-imgBorder"]
    > ![Add tracked keywords and competitors](media/si-app-admin-keywords-and-competitor-tracking.png "Add tracked keywords and competitors")
 
10.	Select **Finish** to complete the setup of conversation intelligence for your organization.

    The status message will be displayed on the top of the page.

    > [!div class="mx-imgBorder"]
    > ![Setup progress message](media/si-app-admin-status-message-set-up.png "Setup progress message")
  
Now your conversation intelligence application is ready, and managers and sellers can use it to view this data.

## Configure in the Sales Hub app

Perform the following steps to configure conversation intelligence through the Sales Hub app.

1.	You must have an administrator or equivalent security role. More information: [Assign a security role to a user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user)

2.	Sign in to Dynamics 365 Sales, and go to the **Sales Hub** app.

3.	Select the **change area** ![change area](media/change-area-icon.png) <!--note from editor: Okay to use the icon here? I thought it would be a nice touch.--> in the lower-left corner of the page, and then select **Sales Insights settings**. 

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings")

4.	On the configuration page, under **Productivity**, select **Conversation intelligence**. 

    > [!div class="mx-imgBorder"]
    > ![Conversation intelligence configuration page](media/ci-admin-config-page.png "Conversation intelligence configuration page")

5.	In the **Call recording storage** section<!--note from editor: It's either "in the **Call recording** section.." or "under **Call recording**..." -->, configure the storage-related options as follows:

    - **Storage location**: Enter the **Storage connection string** and **Container name** to upload the call recordings for analysis. More information: [Configure conversation intelligence to connect call data](../sales/configure-conversation-intelligence-call-data.md)

    - **Retention policy**: Choose a time limit for data retention. The application retains call recording data for the specified time limit and deletes it when the time limit is reached. More information: [Retention Policy](data-retention-deletion-policy.md#retention-policy)

    > [!div class="mx-imgBorder"]
    > ![Configuration call recording storage](media/ci-admin-connection-storage.png "Configuration call recording storage")

6.	In the **Conversation tracking** section, add the keywords and competitors that you want to track on the call. You can update these keywords and trackers later when your organization's requirements change. Also, you can add languages that the sellers might use during their calls with customers. More information: [Configure keywords, competitors, and languages in Conversation content](../sales/configure-keywords-competitors.md)

    > [!div class="mx-imgBorder"]
    > ![Configuration conversation trackers](media/ci-admin-conversation-trackers.png "Configuration conversation trackers")

    >[!NOTE]
    >-	Storage and conversation tracking are the only required fields for first-time onboarding to conversation intelligence. If you'd like, you can publish these settings if you want (skip to step 11). 
    >-	Sales managers can configure the conversation trackers specific to their team.

7.	In the **Sales team management** section, configure the top sellers and hierarchy options as follows:

    - **Call data visibility**: Select the levels of hierarchy for which sales managers can view conversation intelligence data.

    - **Team members and top performers**: You can view the names of your team members whose calls are being analyzed in conversation intelligence, select your top performers, and delete conversation<!--note from editor: Suggested, otherwise you're implying that you'd be deleting your top performers' data, which I don't think you mean. --> data if necessary.

        You can choose the top performers manually or let the application choose automatically. Select one of the following options:

        - **Manually select top performers**: Choose top performers from the list of sellers. In the **Top performer** column, select the star icon corresponding to a seller. The seller is added to the top performers list, where the seller's data is compared against other sellers. 

        - **Enable automatic identification of top performers**: The application automatically selects the top performers based on the number of leads they qualified or opportunities they won. When you select this option, you choose whether to rank performers **by won opportunities** or **by lead qualification**.<!--note from editor: Suggested.-->

    > [!div class="mx-imgBorder"]
    > ![Choose and configure your sales team](media/ci-admin-choose-sales-team.png "Choose and configure your sales team")

    You can skip configuring this section and add your sales team later, when required. More information: [Configure sales team information in Sales Hub app](../sales/configure-view-your-team-page.md#configure-sales-team-information-in-the-sales-hub-app)

8.	In the **License usage** section, you can view the information about the total call recording processing hours left and used. This information view-only and can't be changed.

    > [!div class="mx-imgBorder"]
    > ![View license usage information](media/ci-admin-license-usage.png "View license usage information")
 
9.	In the **Privacy** section, you can select the check box to allow Microsoft to improve the quality of insights through read-only access to your organization's data in conversation intelligence. This is optional.

    > [!div class="mx-imgBorder"]
    > ![Enable privacy](media/ci-admin-enable-privacy.png "Enable privacy")
 
10.	In the **Coming soon** section, select the **Access new features before they're released to all our customers** check box to turn on the "coming soon" feature.
    
    If you don't want to enable preview features for your organization, skip this step. You can always enable them later. More information: [Enable coming soon features](../sales/enable-preview-features-sales-insights-app.md)

    > [!div class="mx-imgBorder"]
    > ![Enable coming soon features](media/ci-admin-coming-soon-features.png "Enable coming soon features")

11.	Select **Save + publish**.
    
    A message is displayed to accept the terms and conditions. Read the terms and conditions, and the privacy statement, carefully. Select **Agree and continue**.
    
    > [!div class="mx-imgBorder"]
    > ![Agree to terms and conditions to publish the configurations](media/ci-admin-agree-terms-conditions-to-publish.png "Agree to terms and conditions to publish the configurations")

Conversation intelligence is configured and ready for use in your organization.

### See also

[Introduction to administer conversation intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)  
[Prerequisites to use conversation intelligence](prereq-sales-insights-app.md)
