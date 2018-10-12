---
title: "Preview: Data Manager | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/1/2018
ms.reviewer: ""
ms.service: "crm-online"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# Preview: Data Manager

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

## Data Manager Sections
**Those include: Sources, Data, Entities, and Relationships.** Completing those sections will ensure that you loaded all the data that matters to you into Customer 360.  

## Data Manager: Sources
In this section we will explain how to bring data from many of your sources: From CRM systems, to transactional and survey data, to clickstream, social and other data you might have. Connecting your data sources is the first step towards unlocking one of the unique product promises - consolidating and reconciling data on your customers from multiple sources that once were disparate and conflicting. 

- **Step One: Ingesting CRM data**: Upon selecting the **Sources** tab a pop-up window will show up and here you should select **Get Data** for the CRM source you are using as shown below. Both Dynamics 365 and Salesforce are supported by the app. For .csv files (Excel) and other sources, continue to step two.

> [!div class="mx-imgBorder"] 
> ![](media/select-sources-get-data.png "Select Get data")

- **Step Two: Identifying and ingesting additional data sources**: Upon selecting **Learn More** you will view many additional available sources. For locating the specific sources that apply to your organization, first identify their types which are represented by tabs at the top of the page (as shown below). Then, search for your specific sources under the relevant tabs and select **Get Data** for each one of them. Lastly, approve by selecting **Load Data** at the bottom-right corner of the page. If you wish to remove source prior to data ingestion select **Remove Data** for that source.

> [!div class="mx-imgBorder"] 
> ![](media/choose-data-source-menu.png "Data source menu")

## Data Manager: Data

This power query pop-up page can be used to pick and edit specific datasets from your selected datasources. The first button you should use in this page is the ***Bring Data*** button as shown below:

[]

Upon bringing a dataset and choosing it from the left menu (shown below in red), all the dataset fields and attributes appear in the main window (shown in blue). You can filter the dataset by each of the fields (shown in green):

[]

Side by side with the ***Bring Data*** button you will find three more buttons. We will explore these from left to right:
- ***Refresh***: Refreshing the dataset you have selected from the left menu will pull any changes that were made to this dataset at the source. It's recommended to use this functionality with regard to datasets that frequently change.
- ***Options***: 
- ***Combine Tables***: This options enables you to merge two datasets into a single dataset prior to completing the data ingestion

The last functionalty that is available in this page is of editing the 

[]

## Data Manager: Entities
After ingesting the data, you can quickly evaluate how complete and useful it is using the **Entities** page. If you suspect that your ingested data is not complete or useful enough, you can import more data using **Add** button as highlighted below. You can also export the entities table as a .csv file by selecting **Export Data**.

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities-import-data.png "Entities import data")

The ***Entities*** table includes four columns (explored from left to right): 
- **Name**: The names of your data entities. Those may range from Account to Activity to many other categories. Moreover, note that if there is a warning sign next to one of the entities names, it implies that the data for that entity didn't load successfully. 
- **Type**: The types of your data entities. In some cases will be the same as your entities names while in others can be different.
- **Source**: From which datasource this entity was ingested?
- **Actions**: Those include on the entity-level:
    - The possibility to **Edit** this entity
    - The option to 
    - The option to

The app automatically identifies values for these four columns within your ingested data sources and if the identification fails it returns *NA*. Both for *NA* and all the other values, it is recommended to go over the table and make any corrections to it as needed.
