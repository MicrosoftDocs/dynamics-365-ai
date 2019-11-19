---
title: "Create a Customer Insights instance and environments | Microsoft Docs"
description: Create an instance of Dynamics 365 Customer Insights and environments in existing instances.
ms.date: 11/18/2019
ms.service: dynamics-365-ai
ms.topic: "article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Create a Customer Insights instance

This article explains how to create a Dynamics 365 Customer Insights instance and how to provision an environment.

## Sign up for Customer Insights and create the first instance

1. In your browser, go to the [Dynamics 365 Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/) website.

2. Select **Get Started**.

3. Choose your preferred sign-up scenario and select the corresponding link.

4. You may need to accept the terms and conditions and select **Continue** to start creating the instance.

5. After the environment is created, you'll be redirected to [your Customer Insights instance](https://home.ci.ai.dynamics.com).

6. You can use the demo environment to explore the app, or create a new environment. Learn more about specifying the settings to create an environment.

7. After specifying the environment settings, select **Create**.

8. You'll be signed in to Customer Insights when the environment was created successfully.

## Create an environment from an existing Customer Insights instance

1. Select the **Settings** symbol in the header of the app.

2. Select **Environments**.

3. In the panel on the right side of the screen, select **New environment**.

4. Specify the basic and advanced settings and select **Create** to create the environment.

## New environment settings

When you create a new environment, you can specify basic settings, and optionally, some advanced settings.

1. In the **Create new environment** dialog, provide the following details:
   - **Display name**: The name that represents this enviroment in the Customer Insights app
   - **Region**: The region into which the service is deployed and hosted
   - **Type**: Select if you want to create a Production environment or a Sandbox environment

2.	Optionally, you can select **Advanced** to configure additional settings:
a.	In the Advanced settings, you can select the storage where you want to store/write the output data generated from Customer Insights. 
b.	This will have two options, Customer Insights storage and Azure Data Lake Storage Gen2. By default, Customer Insights storage option is selected.
c.	Customer Insights storage option means that all the output entities will be stored in the Customer Insights team managed data lake.
d.	If you wish to save/write the output entities generated out of Customer Insights into your own ADLS Gen2 storage account, select the Azure Data Lake Storage Gen2 option from this dropdown.
Note:
By saving data to Azure Data Lake Storage, you agree that data will be transferred to and stored in the appropriate geographic location for that Azure storage account, which may differ from where data is stored in Dynamics 365 Customer Insights.  Learn more at the Microsoft Trust Center.
Ingested entities will continue to be written to the CI managed data lake. There is no option available currently to write the ingested entities also to the customer’s data lake. That is a future enhancement.

We support only Azure Data Lake Gen2 Hierarchical Name Space (HNS) enabled storage accounts. Non-HNS storage accounts are not supported yet.

e.	Once you select Azure Data Lake Storage Gen2 option, you will see two fields for Account name and Account key to specify your storage account. Notice that the Container name is defaulted to ‘customerinsights’ and cannot be edited. 
 
f.	With this setting, once you start performing operations in Customer Insights like data ingestion, running data unification, creating segments and measures etc., you will notice that the corresponding folders will get created in the storage account folder you specified above, and the data files and model.json files will get created and added to the respective subfolders based on the operations you perform.
g.	If you create multiple instances of Customer Insights and choose to save the output entities from all those instances in your storage account, separate folders will be created for each instance with ci_<instanceid> in the container.
h.	Once you select to save CI output Azure Data Lake Storage Gen2 option and create the instance, you will not be able to revert that setting. You can however update the Access key as needed. If you wish to change the storage option, you will need to delete the instance and create a new instance altogether.
Editing an existing environment setting
1.	Once you create an environment, you can edit the environment details like name etc.
2.	In the Environments panel, click on the ellipsis option and select Edit to edit the environment details.
3.	Only display name can be edited for an environment. Region and Type cannot be edited.
4.	(Preview) If an environment has a setting to save all output entities data to the customer’s Azure Data Lake Storage Gen2 option, only account key can be updated. Account name and Container name cannot be edited.
 
Deleting an existing environment
1.	In the Environments panel, click on the ellipsis option and select Delete to delete an environment.
2.	You will see a confirmation screen to confirm if you want to delete the environment and asks you to type in the environment name.
3.	Once you type in the environment name and click Delete, environment will be deleted, and you will see a confirmation message that the environment is deleted.
