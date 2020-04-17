---
title: "Connect to Dynamics 365 Customer Service environment | MicrosoftDocs"
description: "Connect to the Dynamics 365 Customer Serice environment"
ms.date: 04/20/2020
ms.service: 
 - dynamics-365-ai
ms.custom: 
ms.topic: article
author: lalexms
ms.author: laalexan
manager: shujoshi 
---

# Connect to Dynamics 365 Customer Service environment

The **Data sources** section helps you to disconnect or connect a Dynamics 365 Customer Service environment with call insights. If you have multiple environments in your organization and want to activate another environment to display data in the application, use this section. 

At a time, you can have only one active Dynamics 365 Customer Service environment that is connected to the application. When you activate an environment, the existing environment will automatically deactivate, and the new environment’s data will be displayed on the application. Also, you must add tracked keywords and competitors as well as provide permission to access the data to the added environment.

As an administrator, you must configure the Dynamics 365 Customer Service environment to connect to call insights.

1.	Review the prerequisites. To learn more, see [Prerequisites to configure call insights](ci-admin-prereqs.md).

2.	Open **Call insights (Preview)** in the Customer Service Insights application. 

3.	Select the **Settings** icon on the top-right of the page and then select **Settings**.

    > [!div class="mx-imgBorder"]
    > ![Select settings option](media/si-app-admin-select-settings.png "Select settings option")

4.	On the **Settings** page, select **Data source**. 

    > [!div class="mx-imgBorder"]
    > ![Data source section](media/si-app-admin-select-data-source.png "Data source section")
 
5.	In the **Dynamics 365 environment** section, select **+ Add an environment**.

    > [!div class="mx-imgBorder"]
    > ![Select an environment to add](media/si-app-admin-select-add-an-environment.png "Select an environment to add")
 
6.	In the **Connect your data** dialog box, select your Dynamics 365 Customer Service environment to connect with the application.

    > [!div class="mx-imgBorder"]
    > ![Select Dynamics 365 Customer Service environment](media/si-app-admin-connect-d365-organization.png "Select Dynamics 365 Customer Service environment")

    The application now detects your environment.

7.	In the **Terms and conditions** dialog box, accept the terms and conditions, and select **Agree and continue**.

    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions](media/si-app-admin-accept-tandc.png "Accept terms and conditions")
 
    The application takes few minutes to connect your data with the application, and a progress dialog box is displayed.

    > [!div class="mx-imgBorder"]
    > ![Environment connection progress](media/si-app-admin-connection-progress-d365-org.png "Environment connection progress")
 
8.	In the **Create an application user** dialog box, select **Grant permissions** to create an application user.

    > [!div class="mx-imgBorder"]
    > ![Grant permissions to create application user](media/si-app-admin-grant-permission-create-app-user.png "Grant permissions to create application user")
 
    > [!NOTE]
    > If you have already added this environment, the step to grant permissions for the application to access the data will be skipped.

9.	In the **Connect your call data** dialog box, enter the **Storage connection string** and **Container name**, and then select **Connect**. To learn more on how to get the **Storage connection string** and **Container name** values, see [Configure conversation intelligence to connect call data](configure-conversation-intelligence-call-data.md).

    > [!div class="mx-imgBorder"]
    > ![Enter values to connect call data](media/si-app-admin-connect-call-data.png "Enter values to connect call data")
 
10.	In the **Keyword and product tracking** dialog box, add the keywords and products that you want to track on calls. You can update these keywords and trackers later when your organization requires a change. To learn more, see [Configure keywords and products to track](ci-admin-config-keywords-products.md).

    > [!div class="mx-imgBorder"]
    > ![Add tracked keywords and products](media/si-app-admin-keywords-and-product-tracking.png "Add tracked keywords and competitors")
    
   > [!NOTE]
   > You can skip adding the keywords and competitors and add them later, when required.

11.	Select **Finish** to complete the setup of the **Conversation Intelligence** application for your organization. The status message will be displayed on the top of the page.

    > [!div class="mx-imgBorder"]
    > ![Set up progress message](media/si-app-admin-status-message-set-up.png "Set up progress message")
  
Now, your call insights feature is ready with the data of the added environment.

### See also

[Introduction to administer Conversation Intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)

[Prerequisites to configure Conversation Intelligence](ci-admin-prereqs.md)
