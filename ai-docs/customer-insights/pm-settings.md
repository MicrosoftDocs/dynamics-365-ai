---
title: "System | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 11/26/2019
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
author: m-hartmann
ms.author: mhart
manager: shellyha
---
# System

The **System** page contains everything that administrators need to closely monitor the various processes running behind the scenes of Customer Insights. It includes four tabs: **Status**, **Schedule**, **About**, and **General**.

> [!div class="mx-imgBorder"]
> ![System page](media/system-tabs.png "System page")

> [!NOTE]
> If your data sources are updated on a regular basis, we highly recommend that you use the **Schedule** tab. Make sure to review the "Schedule tab" section later in this topic.

## Status tab

The **Status** tab lets you track the progress of data ingestion as well as several important product processes. User this to ensure the completeness of any major process you've defined in Customer Insights. This tab includes two tables:

- **Data sources**: This table lists all the data sources from which you are ingesting your data. The left-side column specifies the names of those data sources. The middle column shows the status of ingestion for each of the data sources:
  - Didn't start
  - In progress
  - Already completed
  
   The right-side column shows the last data refresh date for each of the data sources.

    > [!div class="mx-imgBorder"]
    > ![System data sources](media/system-data-sources.png "System data sources")

- **System processes**: This table lists all the processes that should be executed in Customer Insights to create a unified customer profile. The left-side column specifies the names of those processes. The middle column shows the status of progress for each of the processes:
  - Didn't start
  - In progress
  - Already completed
  
    The right-side column shows the last data refresh date for each of the processes.

    > [!div class="mx-imgBorder"]
    > ![Refresh date](media/system-status-processes.png "Refresh date")

You can view the details of each completed data source ingestion or system process by selecting that item.

## Schedule tab

Use the **Schedule** tab to schedule automatic refreshes of all your ingested Customer Insights data. This helps to ensure that updates from your data sources are reflected in your unified customer profile.

In Customer Insights, the default state for data refreshes is **Off**. To enable scheduled refreshes, first change the toggle at the top of the screen to **On**.

> [!div class="mx-imgBorder"]
> ![System data refresh on](media/system-data-refresh-on.png "System data refresh on")

Next, choose between **Weekly** (default) and **Daily** refreshes. If you intend to schedule weekly refreshes, select one or more days on which you want to run the refresh.

Select the **Time** field. In the timer dropdown, use the arrows to set your refresh timing. When you are finished, select **Set**. You can also **Close** the timer without saving your choices.

If you'd like to schedule multiple refreshes in a single day, select **Add another time**. You can discard any of your set timings by clicking the **X** to the right of the field.

When you're done, don't forget to **Save** your changes.

## About tab

> [!div class="mx-imgBorder"]
> ![About tab](media/system-data-about-tab.png "System data About tab")

The **About** tab contains your organization's **Display name**, as well as the active **Instance name** and **Region**. If you have more than one work instance, it is recommended that you give each an easily identifiable name.

## General tab

Only one option, **Language**, is currently available on the **General** tab. Supported languages appear in this menu. Don't forget to **Save** your selection.

> [!div class="mx-imgBorder"]
> ![General tab](media/system-tabs-general.png "General tab")
