---
title: "Configure call intelligence for Dynamics 365 AI for sales | MicrosoftDocs"
description: "Configure call intelligence in Dynamics 365 AI for sales app"
keywords: "Call intelligence, Dynamics 365 AI for sales, AI for sales, Sales AI"
ms.date: 12/06/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 5fbbe749-6b23-49a6-91a1-0499f9a4fb92
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Configure Call intelligence

Applies to Dynamics 365 Customer Engagement, version 9.1.0 <br>

The call intelligence in Dynamics 365 Customer Engagement assists the sales managers in your organization to view and assess the overall team performance and individual performance of sales reps. This helps in changing the shape of your business by improving sales and generate revenue. 
As an administrator, you must configure the call intelligence in your organization for sales managers to use. Perform the following steps to configure the call intelligence:
1. Review the prerequisites. 
2. Create a Blob container on Azure.
3. Configure blob container and trackers with call intelligence.

## Prerequisites
Verify the following requirements before configuring call intelligence for your organization:
1. You have access to Dynamics 365 AI for sales app.
    If you do not have access, follow these steps:<br>
    a. Go to [Dynamics Sales AI](https://aka.ms/salesai) marketing page and select **Try Preview**.<br>
    b. Enter your work email address.<br>
    c. When the application recognizes the email, you must sign in using Azure Active Directory.<br> 
        [!INCLUDE[proc_more_information](../includes/proc-more-information.md)][Azure AD Connect user sign-in options](/azure/active-directory/hybrid/plan-connect-user-signin).
2. Create a V2 storage account with Azure subscription. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)][Create a storage account](/azure/storage/common/storage-quickstart-create-account?tabs=portal#create-a-storage-account-1).

## Create storage account
Follow the steps below to create a new container in an Azure storage account:
1. Log in to Azure dashboard.
2. On the navigation pane, select **All Resources** and open the desired storage account.
3. From **Services**, select **Blobs**.
4. Select **+ Container** and enter the container information such as name and public access level.
5. Select **OK**.
    The container is created. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)][Create a container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).<br> 
Now, you are ready to upload the call files into the created blob storage container.

## Configure blob container and trackers for call intelligence 
Configuring the blob container that you have created using Azure helps you to fetch the call recording files from your folder and send them to the blob storage for analysis. The analysis includes creating transcripts and provide insights for the call recordings.

You can upload the recording files in audio formats such as mp3 and wav. Along with the audio format file you must upload the corresponding metadata file in JSON format with same name as the uploaded audio file.

Also, you should configure keywords and competitors that you would like to track in the calls. These keywords are also known as trackers. Whenever the defined keywords or competitors are mentioned in a call, the application will gather the data and displays appropriately on the Call intelligence dashboard.

Follow these steps:

1. Open [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] app. 
2. When you are logging in to the app for the first time, the app prompts you to select your Dynamics 365 organization. Select your organization and continue.
3. (Optional) If you do not have a Dynamics 365 organization, select **Setup call intelligence for call center** and continue to configure **Call intelligence** with following steps:<br>
    a. On **Telephony setup** page, enter **Azure storage connection string** and **Container name** that you have configured in Azure.<br>
    b. Select **Proceed to tracker setup**.<br>
    c. On **Trackers setup** page, add **Custom trackers** and **Competitors** that you want to track during calls.<br>
    d. Select **Get started**.<br>
    The call intelligence is configured, and your users are ready to use the feature.
4. Select settings icon at the top-right of the page. 
5. On **Call intelligence** configuration page, enter the information as required:
    - **Azure storage connection string:** Specifies the string that is generated while creating the blob storage account.
    - **Container name:** Specifies the name of the blob storage.
    - **Customer trackers:** Specifies the keywords to track during a call.     For example, when a sales executive makes a sales call, you would like to track keywords such as pricing, budget, potential, and savings.
    - **Competitors:** Specifies names of your competitors or competitive products that may come up during a call with your customers.
6. Select **Save changes**.


### See also

[Analyze customer calls](../sales/call-intelligence.md)
