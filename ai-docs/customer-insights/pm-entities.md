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

After ingesting your data using the **Data Sources** page, you can quickly evaluate how complete and useful it is with the **Entities** page.

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities-import-data.png "Entities import data")

<!--note from editor: "Type" is in screen shot, not in list. "Last Refreshed" is in list, not in screen shot.  -->

The **Entities screen** includes seven columns: 
- **Name**: The names of your data entities. Those can range from *Account* to *Activity* to many other categories. Note: If there is a warning sign next to an entity name, it implies that the data for that entity didn't load successfully. 
- **Source**: Answers the question *From what data source was this entity ingested?* (for example, a CSV file or Azure data source).
- **Created By**: Answers the question: *By whom was this entity originally created?*
- **Created**: Answers the question: *When was this entity created?*
- **Updated By**: Answers the question: *By whom was this entity's data updated?*
- **Last Updated**: Answers the question: *When was the last time this entity's data was updated?*
- **Last Refreshed**: Answers the question: *When was the last time this entity's data was refreshed?*

## Exploring a specific entity's data

Select an entity to explore the different fields and records included within that entity.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-data.png "Data manager entities")

- When you open the **Entities** page, the **Data** tab is selected by default (outlined in the preceding image), and the **Data** table appears below it. This table provides details about each of this entity's records, including the record's value, when it was created, and when it was last refreshed.

- After selecting the **Fields** tab, the **Fields** table appears. You can use this table to view all the details for the selected entity, such as field names, data types, and types. Items in the **Type** column are  Common Data Model-associated types, which can differ from those records' data types if those are not Common Data Model-related.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-fields.png "Data manager fields")

Both the **Fields** table and the **Data** table show only a sample of your entity's data. In order to view the full data set, go to the **Data sources** page, select your entity of interest, select **Edit**, and then view this entity's data within the Power Query editor as explained in [Data sources](pm-data-sources.md).

## Next step

Continue to the **Configure data** section, where you will learn how to complete the three mandatory data configuration phases: *Map*, *Match*, and *Merge*.
