---
title: "Get data | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/13/2019
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
---
# Data Manager: Entities

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

After ingesting your data using the **Data sources** page, you can quickly evaluate how complete and useful it is with the **Entities** page. If you suspect that your ingested data is not complete or useful enough, you can import more data using the **Import Data** button.

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities-import-data.png "Entities import data")

The **Entities screen** includes seven columns: 
- **Name**: The names of your data entities. Those may range from *Account* to *Activity* to many other categories. Note: If there is a warning sign next to an entity name, it implies the data for that entity didn't load successfully. 
- **Source**: Answers the question *From what data source was this entity ingested?* (for example: CSV file, Azure data source, etc.).
- **Created by**: Answers the question: *By whom was this entity originally created?*
- **Created**: Answers the question: *When was this entity created?*
- **Updated By**: Answers the question: *By whom was this entity's data updated?*
- **Last Updated**: Answers the question: *"When was the last time this entity's data was updated?*
- **Last Refreshed**: Answers the question: *When was the last time this entity's data was refreshed?*

## Exploring a specific entity's data

Select an entity to explore the different fields and records included within that entity.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-data.png "Data manager entities")

- When you open the **Entities** page, the **Data** tab will be selected by default (shown in red above) and the **Data table** will show below it. This table provides details around each of this entity's records, including the record's value, when it was created, and when was it last refreshed.

- After selecting the **Fields** tab, the **Fields table** will show up. You can use this table to view all the details for the selected entity, such as fields' names, data types and types. Types stands for CDM-associated types and hence can differ from those records' data types if those are not CDM-related.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-fields.png "Data manager fields")

Both the **Fields table** and the **Data table** show only a sample of your entity's data. In order to view the full data set, go to the **Data Sources** page, select your entity of interest, select **Edit**, and then view this entity's data within the power query editor as explained in [Data Sources](pm-data-sources.md).

## Next Step

Continue to the **Configure data** section where you will learn how to complete the three mandatory data configuration phases: *Map*, *Match* and *Merge*.
