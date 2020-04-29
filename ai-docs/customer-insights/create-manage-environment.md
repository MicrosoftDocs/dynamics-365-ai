---
title: "Manage environments in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Create and manage environments in Dynamics 365 Customer Insights."
ms.date: 04/29/2020
ms.service: dynamics-365-ai
ms.topic: "article"
ms.reviewer: adkuppa
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Manage environments

This article explains how to create a Dynamics 365 Customer Insights instance and how to provision an environment.

## Sign up for Customer Insights and create the first instance

1. In your browser, go to the [Dynamics 365 Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/) website.

2. Select **Get Started**.

3. Choose your preferred sign-up scenario and select the corresponding link.

4. You need to accept the terms and conditions and select **Continue** to start creating the instance.

5. After the environment is created, you'll be redirected to [your Customer Insights instance](https://home.ci.ai.dynamics.com).

6. You can use the demo environment to explore the app, or create a new environment. Learn more about specifying the settings to create an environment.

7. After specifying the environment settings, select **Create**.

8. You'll be signed in to Customer Insights when the environment was created successfully.

## Create an environment

1. Select the **Settings** symbol in the header of the app.

2. Select **Environments**.

3. In the panel on the right side of the screen, select **New environment**.

### New environment settings

There are two ways to create a new environment. You can either create an entirely new environment or you can copy some configuration settings from an existing environment.

If you don't want to create a new environment from scratch, select **Copy from existing environment**. You'll see a list of all available environments from your organization where you can copy data from.

### Specify environment settings

1. In the **Create new environment** dialog, provide the following details:
   - **Display name**: The name that represents this environment in the Customer Insights app. This field is already filled in if you copy from an exsiting environment but you can change it.
   - **Region**: The region into which the service is deployed and hosted
   - **Type**: Select if you want to create a Production environment or a Sandbox environment

2. Optionally, you can select **Advanced** to configure additional settings:

   - **Storage**: Specifies where you want to store the output data generated from Customer Insights. You'll have two options: **Customer Insights storage** (an Azure Data Lake managed by the Customer Insights team) and **Azure Data Lake Storage Gen2** (your own Azure Data Lake Storage). By default, the Customer Insights storage option is selected.

   > [!NOTE]
   > By saving data to Azure Data Lake Storage, you agree that data will be transferred to and stored in the appropriate geographic location for that Azure storage account, which may differ from where data is stored in Dynamics 365 Customer Insights. [Learn more at the Microsoft Trust Center.](https://www.microsoft.com/trust-center)
   >
   > Currently, ingested entities are always stored in the Customer Insights managed data lake.
   > We support only Azure Data Lake Gen2 Hierarchical Name Space (HNS) enabled storage accounts. Non-HNS storage accounts aren't supported yet.

   - For the Azure Data Lake Storage Gen2 option, you need to specify **Account name** and **Account key** for your storage account. The container name is always set to **customerinsights** and can't be changed.
     > [!div class="mx-imgBorder"]
     > ![Environment settings for Azure Data Lake Gen2 storage](media/environment-settings-dialog.png)

   When you perform operations in Customer Insights, such as data ingestion or segment creation, corresponding folders will be created in the storage account you specified above. Data files and model.json files will be created and added to the respective subfolders based on the operations you perform.

   If you create multiple instances of Customer Insights and choose to save the output entities from those instances in your storage account, separate folders will be created for each instance with ci_<instanceid> in the container.

### Additional considerations for copy configuration

The following configuration settings are copied:

- Data sources
- Data unification settings
- Relationships
- Measures
- Segments
- User permissions

The following settings are *not* copied:

- Customer profiles
- Data source credentials. You'll have to provide the credentials for every data source and refresh the data sources manually.
- Data sources from Common Data Model folder and Common Data Service managed lake. You'll have to create those data sources manually with the same name as in the source environment.

When you copy an environment, you'll see a confirmation message that the new environment has been created and the configurations are copied over. Select **Go to data sources** to see the list of data sources.

All the data sources will be show a **Credentials required** status. Edit the data sources and enter the credentials to refresh them.

> [!div class="mx-imgBorder"]
> ![Data sources copied](media/data-sources-copied.png)

After refreshing the data sources, go to **Data** > **Unify** where you find settings from the source environment. Edit them as needed or simply select **Run** to start the data unification process and create the unified customer entity.

When the data unification is complete, go to **Measures** and **Segments** to refresh them too.

## Edit an existing environment

You can edit some of the details of existing environments.

1. Select the **Settings** symbol in the header of the app.

2. Select **Environments**.

3. In the Environments panel, select the ellipsis next to the environment you want to edit and select **Edit**.

4. You can update the **Display name** but you can't change **Region** and **Type** of the environment.

5. If an environment is configured to store data in Azure Data Lake Storage Gen2, you can update the **Account key**. However, you can't change **Account name** and **Container** name.

## Delete an existing environment

1. Select the **Settings** symbol in the header of the app.

2. Select **Environments**.

3. In the Environments panel, select the ellipsis next to the environment you want to edit and select **Delete**.

4. To confirm the deletion, enter the environment name and select **Delete**.
