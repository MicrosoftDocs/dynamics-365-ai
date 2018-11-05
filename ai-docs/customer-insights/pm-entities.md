---
title: "Get data | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
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
# Data Manager: Entities

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

After ingesting your data as part of the mandatory **Get Data** phase, you can quickly evaluate how complete and useful it is using the **Entities** page. If you suspect that your ingested data is not complete or useful enough, you can import more data using **Import Data** button as highlighted below:

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities-import-data.png "Entities import data")

The **Entities screen** includes seven columns (explored from left to right): 
- **Name**: The names of your data entities. Those may range from Account to Activity to many other categories. Note:  if there is a warning sign next to an entity name, it implies the data for that entity didn't load successfully. 
- **Source**: Answers the question *From what data source was this entity ingested?* (for example: .csv file, Azure data source, etc.).
- **Type**: The types of your data entities. In some cases this will be the same as your entities' names; in other cases, the types will differ from the name.
- **Created by**: Answers the question: *By whom was this entity originally created?*
- **Created**: Answers the question: *When was this entity created?*
- **Updated By**: Answers the question: *By whom was this entity's data refreshed?*
- **Last Updated**: Answers the question: *"When was the last time this entity's data was refreshed"?*

The app automatically identifies values for four columns pictured above from your ingested data sources and, if the identification fails, it returns *NA*. Both for *NA* and all the other values, it is recommended to go over the table and make any corrections to it as needed.

## Exploring a specific entity's data
Select an entity to explore the different fields and records included with that entity.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-data.png "Data manager entities")

- When you open the Entities page, the **Data** tab is selected by default. The **Data table** provides details around each of this entity's records including the record's value, when it was created, and when was it was last refreshed.

- When you select the **Fields** tab, the **Fields table** opens. This table shows the details of each of this entity's fields, including the field's name, data type, and type. For the data shown below no types were identified but for other datasets, types may be identified. **Types** stand here for CDM-associated types and hence can differ from those records' **data types** which are not CDM-related.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-fields.png "Data manager fields")

Both the Fields table and the Data table show only a sample of your entity's data. In order to view the full data set, go to the **Get Data** page, select the entity, select **Edit**, and then view this entity's data within the power query editor as explained in the "Get Data" section.
