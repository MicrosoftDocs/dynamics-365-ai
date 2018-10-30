---
title: "Get data | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/1/2018
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

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

# Data Manager: Entities
After ingesting the data, you can quickly evaluate how complete and useful it is using the **Entities** page. If you suspect that your ingested data is not complete or useful enough, you can import more data using **Import Data** button as highlighted below. 

// Replace with entities 1:

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities-import-data.png "Entities import data")

The ***Entities*** screen includes seven columns (explored from left to right): 
- **Name**: The names of your data entities. Those may range from Account to Activity to many other categories. Moreover, note that if there is a warning sign next to one of the entities names, it implies that the data for that entity didn't load successfully. 
- **Source**: Answers the question *From what datasource this entity was ingested?* (csv file, Azure datasource, etc)
- **Type**: The types of your data entities. In some cases will be the same as your entities names while in others can be different.
- **Created by**: Answers the question: *By who this entity was originally created?*
- **Created**: Answers the question: *When was this entity created?*
- **Updated By**: Answers the question: *By who this entity's data was refreshed?*
- **Last Updated**: Answers the question: *"When was the last time this entity's data was refreshed"?*

The app automatically identifies values for these four columns within your ingested data sources and if the identification fails it returns *NA*. Both for *NA* and all the other values, it is recommended to go over the table and make any corrections to it as needed.

## Exploring a specific Entity's data
If you wish to explore the different fields and records that one of your entities includes click that entity. That will take you to the following screen:

[entities 2]

- Upon entering the screen the ***Data*** tab is already opened (as highlighted above). This table enables you to view the details of each of this entity's records. That includes the record's value, when it was created and when was it was last refreshed.

- Upon clicking the ***Fields*** tab, the Fields table will open (as highlighted below). This table enables you to view the details of each of this entity's fields, including the field's name, data type and type (for the data shown below no types were identified but for other datasets types may be identified)

[entities 3]

**Final Note**: Both the **Fields** and **Data** tables show only a sample of your entity's data. In order to view the full data set please go back to the **Get Data** screen, click the entity, click **Edit**, and then view this entity's data within the power query editor as explained in the **Get Data** section.
