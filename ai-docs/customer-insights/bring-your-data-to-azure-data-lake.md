---
title: "Connect Common Data Model data to an Azure Data Lake Gen2 account | Microsoft Docs"
description: Work with Common Data Model data in Dynamics 365 Customer Insights using Azure Data Lake storage.
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

# Connect to a Common Data Model using an Azure Data Lake Gen2 account

This article provides information on how to connect a Common Data Model with Dynamics 365 Customer Insights using your Azure Data Lake Storage Gen2 account.

## Important considerations

- Data in your Azure Data Lake needs to follow the Common Data Model standard. Other formats aren't supported at the moment.

- Customer Insights supports Azure Data Lake *Gen2* storage accounts exclusively. You can't use Azure Data Lake Gen1 storage accounts in Customer Insights.

- Data stored in an online service such as Azure Data Lake Storage may be stored in a different location than where data is processed or stored in Dynamics 365 Customer Insights. By importing, or connecting to, data stored in an online service such as Azure Data Lake Storage, you agree that data can be transferred to, and stored with, Dynamics 365 Customer Insights. [Learn more at the Microsoft Trust Center.](https://www.microsoft.com/trust-center)

## Connect to a Common Data Model folder

1. In Customer Insights, go to **Data** > **Data sources**.

2. Select **Add data source**.

3. Select **Connect to a Common Data Model folder** and select **Next**.

4. Enter a **Name** for the data source and select **Next**.

5. Provide the **Account name**, the **Access key**, and the **Container** for your Azure Data Lake storage and select **Next**.

6. In the **Select a Common Data Model folder** dialog, select the model.json file from the list that you want to use to import the corresponding entities into Customer Insights and select **Next**.
   > [!NOTE]
   > Any model.json file associated with another data source in the instance won't show in the list.

7. You'll get a list of available entities from the selected model.json file. You can review the entities and select **Save**. All of the listed entities will be attached to Customer Insights.

8. After saving your selections, the **Data sources** page opens and you can see the newly added Common Data Model folder connection as a data source.

> [!NOTE]
> A model.json file can only associate with one data source in the same instance. However, the same model.json file can be used for data sources in multiple instances.

## Edit a Common Data Model folder data source

If you would like to update the access key for the storage account that contains Common Data Model folder you connected to, click on the ellipsis, and select Edit option. 

You will see the storage details screen and notice that the Account name and Container are disabled, and Access key is enabled for any edits or updates.  

Account name and container cannot be edited on a data source. 

If you want to connect to a different container from your storage account, you will need to create a new data source connection. 

Alternatively, if you would like to select a different model.json file from the container, you may do so by clicking Next in the Storage details page without any edits and go to the Common Data Model folder screen and select a different model.json file and therefore a different set of entities. 

If there are any downstream dependencies on the existing model.json file and the set of entities, you will receive an error message about the dependency and that you cannot select a different model.json file. If you were to continue to select a new model.json file, you need to remove those dependencies, and then you can select a new model.json file and the entities to be used in CI. 

If you cannot remove the downstream dependencies, we recommend creating a new data source and attach this model.json. 