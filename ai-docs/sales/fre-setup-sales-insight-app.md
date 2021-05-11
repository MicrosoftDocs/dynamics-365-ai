---
title: "First-run setup experience for conversation intelligence | MicrosoftDocs"
description: "First-run setup experience for conversation intelligence"
ms.date: 02/04/2021
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

# First-run setup experience for conversation intelligence with Microsoft Teams in Dynamics 365

You can configure conversation intelligence with Microsoft Teams by completing the following section:      
- [The conversation intelligence application](#the-conversation-intelligence-application)    
- [The Sales Hub app](#the-sales-hub-app)    
- [Microsoft Teams for conversation intelligence](#microsoft-teams-conversation-intelligence)    

After you sign in to conversation intelligence or your sales app, you can set up the conversation intelligence depending on the role that's assigned to you.      
- As an administrator, you can set up the complete application&mdash;including enable Microsoft Teams call recording for conversation intelligence preview, select storage, grant app permissions, and define organization level tracked keywords and competitors to be used by conversation intelligence.     
- As a sales manager or a seller, you will need an administrator to configure the application so you can view the data and settings that are relevant to you. More information: [Configure sales team level settings](configure-sales-team-level-settings.md)

## The conversation intelligence application

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
    >Selecting the first check box allows Microsoft to collect your organization's data to improve the quality of insights. This is optional. 
    The application takes a few minutes to connect to your data, during which a progress dialog box is displayed.
    > [!div class="mx-imgBorder"]
    > ![Environment connection progress](media/si-app-admin-connection-progress-d365-org.png "Environment connection progress")    
6.	In the **Connect your call data** dialog box, enter the **Storage connection string** and **Container name**, and then select **Connect**. More information: [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md)  
    > [!div class="mx-imgBorder"]
    > ![Enter values to connect call data](media/si-app-admin-connect-call-data.png "Enter values to connect call data")   
7.	If you want to turn on access to preview features, in the **Coming soon** dialog box, select the check box and then select **Agree and continue**.  
    > [!div class="mx-imgBorder"]
    > ![Turn on preview features](media/si-app-admin-enable-preview-feature.png "Turn on preview features")   

    > [!NOTE]
    > If you don't want to enable the preview feature for your organization, skip this step. You can always enable preview features later. More information: [Enable coming soon features](enable-preview-features-sales-insights-app.md)  
8.	In the **Keyword and competitor tracking** dialog box, add the keywords and competitors that you want to track on the call. You can update these keywords and trackers later if your organization's requirements change. More information: [Configure conversation content](../sales/configure-keywords-competitors.md)      
    > [!NOTE]
    > You can also skip adding the keywords and competitors at this point. You can always add them later.  
    
    > [!div class="mx-imgBorder"]
    > ![Add tracked keywords and competitors](media/si-app-admin-keywords-and-competitor-tracking.png "Add tracked keywords and competitors")   
9.	Select **Finish** to complete the setup of conversation intelligence for your organization.
    The status message will be displayed at the top of the page.  
    > [!div class="mx-imgBorder"]
    > ![Setup progress message](media/si-app-admin-status-message-set-up.png "Setup progress message")

Now your conversation intelligence application is ready, and managers and sellers can use it to view this data.

## The Sales Hub app

Perform the following steps to configure conversation intelligence through the Sales Hub app.

1.	You must have the Dynamics 365 system administrator or equivalent security role. More information: [Assign a security role to a user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user)  
2.	Sign in to Dynamics 365, and go to your sales app.  
3.	Select the **change area** ![change area](media/change-area-icon.png) in the lower-left corner of the page, and then select **Sales Insights settings**.  
    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings")  
4.	On the configuration page, under **Productivity**, select **Conversation intelligence**.  
    > [!div class="mx-imgBorder"]
    > ![Conversation intelligence configuration page](media/ci-admin-config-page.png "Conversation intelligence configuration page")  
5.	In the **Call recording storage** section, configure the storage-related options as follows:  
    - **Storage location**: Enter the **Storage connection string** and **Container name** to upload the call recordings for analysis. More information: [Configure conversation intelligence to connect call data](../sales/configure-conversation-intelligence-call-data.md).    

        >[!NOTE]
        >By default, the Microsoft provided storage is selected, and we recommend that you use this storage.   

    - **Retention policy**: Choose a time limit for data retention. The application retains call recording data for the specified time limit and deletes it when the time limit is reached. More information: [Retention Policy](data-retention-deletion-policy.md#retention-policy)  
    > [!div class="mx-imgBorder"]
    > ![Configuration call recording storage](media/ci-admin-connection-storage.png "Configuration call recording storage")  
6.	In the **Conversation tracking** section, add the keywords and competitors that you want to track on the call. You can update these keywords and trackers later when your organization's requirements change. Also, you can add languages that the sellers might use during their calls with customers. More information: [Configure conversation content](../sales/configure-keywords-competitors.md)    
    > [!div class="mx-imgBorder"]
    > ![Configuration conversation trackers](media/ci-admin-conversation-trackers.png "Configuration conversation trackers")  
    >[!NOTE]
    >- Storage and conversation tracking are the only required fields for first-time onboarding to conversation intelligence. Steps 7 to 10, including, are optional. You can choose to configure now or later when required. If you choose to configure these settings later, you can skip to step 11. 
    >- Sales managers can configure the conversation trackers specific to their team.  

7.	In the **Sales team management** section, configure the top sellers and hierarchy options as follows:  
    - **Call data visibility**: Select the levels of hierarchy for which sales managers can view conversation intelligence data. 
    - **Team members and top performers**: You can view the names of their team members whose calls are being analyzed in conversation intelligence, select their top performers. You can choose the top performers manually, or let the application choose them automatically. Select one of the following options:  
        - **Manually select top performers**: Choose top performers from the list of sellers. In the **Top performer** column, select the star icon corresponding to a seller. The seller is added to the top performers list, where the seller's data is compared against other sellers.
        - **Enable automatic identification of top performers**: The application automatically selects the top performers based on the number of leads they qualified or opportunities they won. When you select this option, you choose whether to rank performers **by won opportunities** or **by lead qualification**.   
    You can skip configuring this section and add your sales team later, when required. More information: [Configure and view your team page](../sales/configure-view-your-team-page.md).

    > [!div class="mx-imgBorder"]
    > ![Choose and configure your sales team](media/ci-admin-choose-sales-team.png "Choose and configure your sales team")  

8.	In the **License usage** section, you can view the information about the total call recording processing hours left and used. This information view-only and can't be changed.  
    > [!div class="mx-imgBorder"]
    > ![View license usage information](media/ci-admin-license-usage.png "View license usage information")   
9.	In the **Privacy** section, you can select the check box to allow Microsoft to improve the quality of insights through read-only access to your organization's data in conversation intelligence. This is optional.  
    > [!div class="mx-imgBorder"]
    > ![Enable privacy](media/ci-admin-enable-privacy.png "Enable privacy")   
10.	In the **Coming soon** section, select the **Access new features before they're released to all our customers** check box to
    enable preview features for your organization. If you prefer not to enable preview features at this time, skip this step. You can always enable them later. More information: [Enable coming soon features](../sales/enable-preview-features-sales-insights-app.md)  
    > [!div class="mx-imgBorder"]
    > ![Enable coming soon features](media/ci-admin-coming-soon-features.png "Enable coming soon features")  
11.	Select **Save + publish**.      
    A message is displayed to accept the terms and conditions. Read the terms and conditions, and the privacy statement, carefully. Select **Agree and continue**.      
    > [!div class="mx-imgBorder"]
    > ![Agree to terms and conditions to publish the configurations](media/ci-admin-agree-terms-conditions-to-publish.png "Agree to terms and conditions to publish the configurations")  

Conversation intelligence is configured and ready for use in your organization.

## Microsoft Teams for conversation intelligence

> [!IMPORTANT]
> - The enhanced experience for Microsoft Teams together with conversation intelligence is a preview feature. [!INCLUDE[cc-preview-features-definition](../includes/cc-preview-features-definition.md)]
> - [!INCLUDE[cc-preview-features-expect-changes](../includes/cc-preview-features-expect-changes.md)]
> - [!INCLUDE[cc-preview-features-no-ms-support](../includes/cc-preview-features-no-ms-support.md)] 

Using Microsoft Teams together with conversation intelligence in Dynamics 365 Sales helps organizations transform customer interactions into revenue. Calling with Microsoft Teams allows business critical insights to be surfaced both in real-time (during the call), as well as post-call, and are seamlessly tied to the relevant Dynamics 365 records.

### Review the prerequisites

Review the following requirements before you configure Microsoft Teams call recording for conversation intelligence:

- You must purchase a [Dynamics 365 Sales Insights](https://portal.office.com/signup/logout?OfferId=5be85c9f-df71-4bcf-ac2f-b2a05b4a1f99&ali=1) or Sales Premium license 
- You must have a Dynamics 365 system administrator or equivalent security role. More information: [Assign a security role to a user](https://docs.microsoft.com/power-platform/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user)
- Your organization has a Microsoft Teams phone system installed with a valid license to use it. More information: [Set up Phone System in your organization](https://docs.microsoft.com/MicrosoftTeams/setting-up-your-phone-system)
- You have a license to use Microsoft Teams. More information: [Microsoft Teams add-on licenses](https://docs.microsoft.com/MicrosoftTeams/teams-add-on-licensing/microsoft-teams-add-on-licensing?tabs=small-business)
 
### Enable calling with Microsoft Teams 

Before you can proceed to configuring Microsoft Teams with conversation intelligence, you must enable the Microsoft Teams dialer for your organization. More information: [Configure Microsoft Teams dialer](/sales-enterprise/configure-microsoft-teams-dialer). 
 
### Run the PowerShell script to record calls

Before you configure the Teams dialer, run the PowerShell script to enable recording of your Microsoft Teams calls. These call recordings are used for processing and analysis. The PowerShell script creates:
- An Azure Active Directory (Azure AD) security group for which the recording will be enabled
- Microsoft Teams call recording–related artifacts, such as service principal and recording policy

Follow these steps:   
1. [Download the PowerShell script](#download-the-powershell-script)   
2. [Configure the PowerShell script](#configure-the-powershell-script)   

#### Download the PowerShell script

1.	Sign into the Dynamics 365 Sales Hub app as an Dynamics 365 system administrator.    
2.	Select the **change area** ![change area](media/change-area-icon.png) in the lower-left corner of the page, and then select **Sales Insights settings**.  
    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings")   
3.	On the site map, under **Productivity** > **Conversation intelligence**.   
    The conversation intelligence home page opens.   
    > [!div class="mx-imgBorder"]
    > ![Conversation intelligence home page](media/ci-admin-getting-started-page.png "Conversation intelligence home page")   
4.	On the home page, select **Get started**.   
    The conversation intelligence configuration page opens.
5.	In the **Microsoft Teams Call Recording** section, the application validates the successful configuration of the **Microsoft Teams** dialer, and the **PowerShell script**.    
    > [!div class="mx-imgBorder"]
    > ![Download PowerShell script](media/ci-admin-download-powershell-script.png "Download PowerShell script")    
6.	Select **Download** to download the PowerShell script to your local computer.   

#### Configure the PowerShell script

>[!IMPORTANT]
>You must have tenant administrator privileges to run the PowerShell script. 
  
1.	Open a PowerShell command window as administrator and verify that you have the latest PowerShell version. Run the following commands:
    -	`Install-PackageProvider -Name NuGet -Force`
    -	`Install-Module -Name PowerShellGet -Force -AllowClobber`
2.	Install the dependencies by running the following commands:    
    -	`Install-Module -Name MicrosoftTeams -RequiredVersion 1.1.6 -Force -AllowClobber`
    -	`Install-Module AzureAD`
    -	`Install-Module MSAL.PS`     
3.	To run the script, enter the following command:     
    ```.\MediaRecordingTenantProvisioning.ps1```     
    The package starts installing and a sign-in dialog box opens.     
4.	Enter your tenant administrator credentials to sign into your organization.
    >[!NOTE]
    >You’ll be asked to provide credentials thrice.       

	The script installs.     
5.	Go back to Sales Hub app and select **Check status** to validate the successful installation.

You can proceed to configure the Microsoft Teams with conversation intelligence.

>[!NOTE]
><a name="teams-tenant-admin-contact"></a>If any of the validations fail, you can't proceed with the configuration.  
>    -	To set up the phone system and Microsoft Teams for your organization, contact your Microsoft Teams administrator. 
>    -	To run the PowerShell script, contact your tenant administrator. More information: [Configure the PowerShell script](#configure-the-powershell-script) 

### Configure Microsoft Teams call recording

1.	Sign in to Dynamics 365 Sales Hub app.     
2.	Select the **change area** ![change area](media/change-area-icon.png) in the lower-left corner of the page, and then select **Sales Insights settings**.  
    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings")     
3.	On the site map, under **Global settings** > **Productivity** > **Conversation intelligence**.   
    The conversation intelligence home page opens.    
4.	Under the **Microsoft Teams call recordings (preview)** section, enable the preview and then configure the other settings as described in the following table.

    | Option | Description |
    |--------|-------------|
    | Microsoft Teams security roles | Specifies the security roles in your organization who have permission to use the Microsoft Teams dialer. By default, permission is granted to all security roles in your organization. If you want to add or remove security roles, go to [Configure the dialer](https://docs.microsoft.com/dynamics365/sales-enterprise/configure-microsoft-teams-dialer#configure-the-dialer). |
    | Call recording activation | Select an option to initiate call recordings:<ul><li>**Automatically**: Select this option if you want the calls to be automatically recorded when a call is initiated.</li><li>**On demand**: Select this option if you want to allow sellers to start the call recording when a call is initiated.</li></ul>Turn on the **Users can manually stop recording** toggle to allow sellers to stop recording at any point during the call. |
    | Recording notification for customers | Turn on this toggle to notify customers when the call recording is initiated. This lets customers know that the call is being recorded. |

    > [!div class="mx-imgBorder"]
    > ![Enable Microsoft Teams call recording preview](media/ci-admin-enable-teams-preview.png "Enable Microsoft Teams call recording preview")     

    >[!NOTE]
    >Microsoft Teams call recording settings, storage selection, and conversation tracking are required to configure only for first-time onboarding to conversation intelligence. All remaining steps are optional. You can choose to configure them now or later when required.   

5.	(Optional) Under **Call recording storage**, configure the storage-related options as described in the following table.

    | Option | Description |
    |--------|-------------|
    | Storage for call recordings | Select an option to store your call recordings for analysis:<ul><li>**Microsoft provided storage**: Select this option if you want to use the storage provided by Microsoft. By default, this option is selected, and we recommend that you use this storage.</li><li>**Your own Azure storage**: Select this option if you want to use your custom Azure storage. After you select this option, enter the **Storage connection string** and **Container name**.</li></ul> To learn more, go to [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md). |
    | Retention policy | Choose a retention time limit. The application retains call recording data for the specified time limit, and deletes it when the time limit is reached. To learn more, go to [Retention Policy](data-retention-deletion-policy.md#retention-policy). |   

    > [!div class="mx-imgBorder"]
    > ![Select a storage option and retention policy](media/ci-admin-teams-choose-storage-retention-policy.png "Select a storage option and retention policy")

    >[!NOTE]
    >For Microsoft-provided storage, the available retention periods are 30 days and 90 days. If your organization requires longer retention periods, please consider using your own storage.    

6.	Under **Conversation tracking**, add the keywords and competitors that your organization wishes to track during calls, and add the languages used by sellers during calls with customers. 
    This is a global setting that will be applied to all sales calls in the organization. You must set at least one global keyword and at least one global competitor to enable conversation intelligence. You can update these keywords and competitors later if required. More information: [Configure keywords and competitors in Conversation content](configure-keywords-competitors.md). 
        
    > [!div class="mx-imgBorder"]
    > ![Configure conversation tracking](media/ci-admin-conversation-trackers.png "Configure conversation tracking")    
7.	(Optional) In the **Privacy** section, you can select the check box to allow Microsoft to improve the quality of insights with read-only access to your organization's data in conversation intelligence.  
    > [!div class="mx-imgBorder"]
    > ![Enable privacy](media/ci-admin-enable-privacy.png "Enable privacy")   
8.	In the **License usage** section, you can view information about the total call recording processing hours that have been used, and how many available hours remain.       
    > [!div class="mx-imgBorder"]
    > ![View license usage information](media/ci-admin-license-usage.png "View license usage information")   

9.	(Optional) In the **Coming soon** section, select the **Access new features before they're released to all our customers** check box to turn on the "coming soon" feature.      
    If you don't want to enable preview features for your organization, skip this step. You can always enable them later. More information: [Enable coming soon features](../sales/enable-preview-features-sales-insights-app.md)  
    > [!div class="mx-imgBorder"]
    > ![Enable coming soon features](media/ci-admin-coming-soon-features.png "Enable coming soon features")  
10.	Select **publish**.      
    A message is displayed to accept the terms and conditions. Read the terms and conditions, and the privacy statement. Select **Agree and continue**.      
    > [!div class="mx-imgBorder"]
    > ![Agree to terms and conditions to publish the configurations](media/ci-admin-agree-terms-conditions-to-publish.png "Agree to terms and conditions to publish the configurations")    

Microsoft Teams call recording with conversation intelligence is now configured and ready for use in your organization.

### See also

[Introduction to administer conversation intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)  
[Prerequisites to use conversation intelligence](prereq-sales-insights-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]