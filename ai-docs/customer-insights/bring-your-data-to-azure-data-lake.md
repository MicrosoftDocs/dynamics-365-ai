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

- Data stored in an online service such as Azure Data Lake Storage may be stored in a different location than where data is processed or stored in Dynamics 365 Customer Insights. By importing, or connecting to, data stored in an online service such as Azure Data Lake Storage, you agree that data can be transferred to, and stored with, Dynamics 365 Customer Insights. [Learn more at the Microsoft Trust Center.](https://www.microsoft.com/trust-center)

## Connect to a Common Data Model folder

Navigate to Data > Data sources > Click ‘+ Add data source’  

Select the ‘Connect to a Common Data Model folder’ option and click Next 

 

Provide a name to identify this data source and click Next. 

Provide the storage details Account name, Access key and the Container details and click Next. 

 

 

We support only Azure Data Lake Gen2 storage accounts. Azure Data Lake Gen1 storage accounts are not supported. 

 

You will see a list of model.json files available from all the hierarchically specified folders in the container. Note that any model.json file associated with another data source in the instance will not be listed here. 

 

Select a model.json file that you would like to attach the corresponding entities into Customer Insights and click Next. 

You will see the list of entities available from the selected model.json file for your review. 

 

You can review all the entities available and click Save. Currently we do not have an option to select entities from the available list and all the entities will be attached to CI. 

Once you click on Save, you will be taken to the Data sources page and will see the newly added CDM folder connection as a data source. 

A model.json can only associate with one data source in the instance. Meaning, two data sources cannot point to the same model.json file in any given instance. However, a model.json file can be referenced in a data source from multiple instances

## Edit a Common Data Model folder data source

If you would like to update the access key for the storage account that contains Common Data Model folder you connected to, click on the ellipsis, and select Edit option. 

You will see the storage details screen and notice that the Account name and Container are disabled, and Access key is enabled for any edits or updates.  

Account name and container cannot be edited on a data source. 

If you want to connect to a different container from your storage account, you will need to create a new data source connection. 

Alternatively, if you would like to select a different model.json file from the container, you may do so by clicking Next in the Storage details page without any edits and go to the Common Data Model folder screen and select a different model.json file and therefore a different set of entities. 

If there are any downstream dependencies on the existing model.json file and the set of entities, you will receive an error message about the dependency and that you cannot select a different model.json file. If you were to continue to select a new model.json file, you need to remove those dependencies, and then you can select a new model.json file and the entities to be used in CI. 

If you cannot remove the downstream dependencies, we recommend creating a new data source and attach this model.json. 