---
title: "Advanced mode | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 06/17/2019
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
robots: noindex,nofollow
---

# Advanced mode 

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Overview

Advanced mode allows you to use raw SQL data to define any segment. Advanced mode is a capability on the **Segment builder** screen that is described [here](pm-segments.md). 

> [!IMPORTANT] 
>
> - Customer Insights uses the SQL dialect of **Spark 2.3 (HDI 3.6)**. There are minor differences from a raw SQL that you should be aware of before you type the SQL query for your segment.
> - View the SQL guidelines later in this topic.
> - View the Spark 2.3 [documentation](https://spark.apache.org/docs/2.3.0/). 

### When should I use advanced mode? 

Use advanced mode when you want to create a segment that is difficult or impossible to create on the **Segment builder** screen. For example, consider the following scenarios that can't be achieved using the Segment builder:

- Nesting an **AND** operator within an **OR** operator.
- Using operators that don’t exist in the builder, such as **Time** or **Percentile**.
- Using group filters (**Unite**, **Intersect**, and **Exclude**) in ways that are not supported in the builder.
 
For scenarios such as these, you might want to consider using advanced mode. 

### What skills should I have to use advanced mode?

To use advanced mode, you need to be able to (or access someone who can) write a SQL query that produces your segment as an output.

## Get started with advanced mode

There are two ways to enter advanced mode:

- The **Create segment** panel:

  > [!div class="mx-imgBorder"]
  > ![Create segment screen](media/enter-advanced-mode-1.png "Create segment screen")

  > [!NOTE]
  > When you create a segment using advanced mode, all future edits to this segment must be done using advanced mode.

- The **Complete segment definition using SQL** button on the **Segment builder** screen.

  > [!div class="mx-imgBorder"]
  > ![Create segment screen](media/enter-advanced-mode-2.png "Create segment screen")

  > [!NOTE]
  > When you select the **Complete segment definition using SQL** button,  a notification appears that you have to accept to continue. After you accept, you have to perform all future edits to this segment using the advanced mode screen rather than the Segment builder screen.

## The advanced mode screen

The advanced mode screen includes four components.

> [!div class="mx-imgBorder"]
> ![Advanced screen](media/advanced-screen.png "Advanced screen")

1. ***Editor* window**: This is your working area where you enter your SQL query. Your segment output must include all the fields from the *Customer Insights* entity.  This requirement is already fulfilled through the code that is populated on the first line. Note that if you wish to include additional fields in your segment output you need to write a corresponding statement.

2. ***View guidelines* link**: Make sure you know the few differences between a free-format SQL code and the code format used in Customer Insights. The image below shows some of these guidelines as well as an example for a valid SQL query. Make sure to visit the Spark 2.3 [documentation](https://spark.apache.org/docs/2.3.0/) for more details.
 
   > [!div class="mx-imgBorder"]
   > ![SQL guidelines](media/sql-guidelines.png "SQL guidelines")

3. ***Save* button**: Use this button to save and process your segment. If it’s a valid query, it will produce a segment and you should expect to see it in the **Segments** screen. If it’s an invalid query, your segment definition will be saved as a draft. Visit the **Segments** topic for more details on the **Draft mode.**

4. ***Back to segments***: Use this button to go back to the **Segments** screen.

## Edit, rename, or delete a segment

Any segment that you create or edit using advanced mode must also be edited in advanced mode. You cannot use the Segment builder screen to edit these segments. Within the corresponding segment tile on the **Segments** screen, select the ellipses (…) button to show the **Edit**, **Rename**, and **Delete** options. 
