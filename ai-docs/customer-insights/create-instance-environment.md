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

The following steps explain how to create a Customer Insights instance and specify the basic and advanced settings for provisioning an environment.
Creating an instance for the first time
1.	Open a browser and navigate to: https://dynamics.microsoft.com/ai/customer-insights/
2.	Click Get Started
3.	Based on your scenario, you can click on either of the links to start a trial or get access to environments via PartnerSource or login as a Microsoft employee.
 

4.	Once you create an environment from the appropriate channels as above, you will progress to https://home.ci.ai.dynamics.com
5.	You may see a provisioning screen as below for the terms and conditions acceptance.
 

6.	Click on Continue to create the new instance. 
7.	You may be prompted to create a new environment. Refer to Settings section to specify the basic and advanced settings for the instance.
8.	Once you specify the basic and optional advanced settings, click Create button to create the instance.
9.	You will see an intermediate screen while the instance creation happens in the background, and once done, you will be signed into Customer Insights and will be taken to the Customer Insights home page.

Creating an instance from within an existing instance
You can also create a new instance after from an existing instance in the following way
1.	Click on the Settings icon on the top right of the screen and select Environments option.
2.	A new panel will show up from right side of the screen and will display the list of existing instances in your tenant.
3.	On the bottom left part of the panel, you will see an option to create new environment.
4.	Click on ‘+New environment’ link and this will open a new pop up screen to fill in details to create an environment.
5.	Once you specify the basic and optional advanced settings as mentioned in the Settings section, click Create button to create the instance.
6.	You may see an intermediate screen while the instance creation happens in the background, and once done, you will see that the new instance record gets added to the Environments panel on the right side.
Settings

1.	In the pop-up screen, provide a display name, select the region into which you wish to deploy the service and type. Type can be either a Production or a Sandbox instance, depending on your requirement.
 
2.	Advanced settings:
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
