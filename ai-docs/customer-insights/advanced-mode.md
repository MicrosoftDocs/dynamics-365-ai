---
title: "Advanced mode | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 04/01/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
 - "Dynamics 365 (online)"
 - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "dean-haas"
ms.author: "v-dehaas"
manager: "kvivek"
---
# Advanced mode

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Overview

Advanced mode allows you to use raw SQL data to define any segment. Advanced mode is a capability on the **Segment builder** screen that is described [here](pm-segments.md). 

> [!IMPORTANT] 
> - Customer Insights uses the SQL dialect of **Spark 2.3 (HDI 3.6)**. There are minor differences from a raw SQL which you should be aware of before you type the SQL query for your segment. 
> - View the [SQL guidelines](NEED-LINK) later in this topic.
> - View the Spark 2.3 [documentation](NEED_LINK). 

### When should I use advanced mode? 

Use advanced mode when you want to create a segment that is difficult or impossible to create on the **Segment builder** screen. For example, consider the following scenarios:

 - You can't nest an **AND** operator within an **OR** operator in segment builder. 
 - You can't use operators that don’t exist in the segment builder, such as **Time** or **Percentile**. 
 - You can't use group filters in ways that are not supported in the segment builder. 

> [!NOTE]
> To use advanced mode, you need the skill (or access to someone with the skill) to write a SQL query which produces your segment as an output. 

## Using Advanced mode for the first time

> [!NOTE]
> When you create a segment using Advanced mode, you must also perform any edits to this segment using Advanced mode.

There are two entry points into the Advanced mode:

- The **Create segment** panel:
- The **Carry selections to advanced mode** button:
// Image to be completed
**Important note**: Upon selecting the **Carry selections to advanced mode** button you choose to perform all future edits of this segment using the Advanced mode screen rather than the Segment builder screen.

## The Advanced mode screen
As shown below, the Advanced mode screen includes four components:
 
// We should number the components in the image above accordingly..:
- 1. ***Editor* window:** This is your working area - type your SQL query here. Your segment output must include all the fields from the *Customer Insights* entity and, as shown above, this requirement is already fulfilled through the code that is populated on the first line. Note that if you wish to include additional fields in your segment output you will need to write a corresponding statement.
- 2. ***View guidelines* button:** Make sure to know the few differences between a free-format SQL code and the code format used in Customer Insights. The image below shows some of these guidelines as well as an example for a valid SQL query. Make sure to visit the Spark 2.3 documentation for more details.
 
- 3. ***Save** button:* Use this button to save and process your segment. If it’s a valid query, it will produce a segment and you should expect to see it in the **Segments** screen. If it’s an invalid query, your segment definition will be saved as a draft. Visit the **Segments** topic for more details on the **Draft mode.**
- 4. ***Back to segments** button:* Use this button to go back to the **Segments** screen.

## Editing, renaming and deleting your segment
Any segment that you have created or edited using the Advanced mode screen can only be edited using that screen and not the **Segment builder** screen. Within the corresponding segment tile on the **Segments** screen, click the **(…)** button and then click **Edit** to edit your segment. Click **Rename** to rename your segment. Click **delete** to delete your segment.
