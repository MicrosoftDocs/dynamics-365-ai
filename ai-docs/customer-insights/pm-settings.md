---
title: "System | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/26/2019
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
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# System

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The **System** page encapsulates everything that you, as an administrator, need to closely monitor the various processes that run behind the scenes of Customer Insights. As shown here, it includes four parts: **Status**, **Schedule**, **About**, and **General**.

> [!div class="mx-imgBorder"] 
> ![](media/system-tabs.png "System page")

> [!NOTE]
> If your data sources are updated on a regular basis, we highly recommend that you use the **Schedule** tab. Make sure to review "Schedule tab" later in this topic.

## Status tab

The **Status** tab enables you to track the progress of data ingestion as well as several important product processes. With that, you can ensure the completeness of any major process you define in Customer Insights. This tab includes two tables:

- **Data sources**: This table lists all the data sources from which you are ingesting your data. The left-side column specifies the names of those data sources. The middle column shows the status of ingestion for each of the data sources: 
  - Didn't start
  - In progress
  - Already completed
  
   The right-side column shows the last data refresh date for each of the data sources.

    > [!div class="mx-imgBorder"] 
    > ![](media/system-data-sources.png "System data sources")

- **System processes**: This table lists all the processes that should be executed in Customer Insights to create a unified customer profile. The left-side column specifies the names of those processes. The middle column shows the status of progress for each of the processes:
    - Didn't start 
    - In progress 
    - Already completed 
  
  The right-side column shows the last data refresh date for each of the processes.

    > [!div class="mx-imgBorder"] 
    > ![](media/system-status-processes.png "Refresh date")

- In addition, you can view the details of each completed data source ingestion or system process by selecting that data source or system process row. In the following example, the user has selected the **Dynamics** data source that has ingestion status **Completed** (#1). Additional details on that data source are also displayed (#2).

  > [!div class="mx-imgBorder"] 
  > ![](media/system-database-details.png "Data source details")

## Schedule tab

Use the **Schedule** tab to refresh all of your ingested Customer Insights data and to schedule the frequency and timing of the refreshes. As data is constantly updated in some or all of your data sources, it's important to ensure that those updates appear in your unified customer profile. The **Schedule** tab enables you to achieve that automatically.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-off.png "System data refresh off")

In Customer Insights, the default state for data refresh is **Off**, reflecting no scheduled refreshes (as shown in the preceding example). To allow scheduled refreshes, change the toggle at the top of the screen to **On**, as shown in the following example.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-on.png "System data refresh on")

The next step is to decide between **Weekly** (default) and **Daily** refreshes.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-period.png "System data refresh period")

**To schedule a daily refresh:**

1. Select the **Time** field.

   > [!div class="mx-imgBorder"] 
   > ![](media/system-data-refresh-time-period.png "System data refresh time period")

2. In the timer shown in the preceding example, use the four arrows to set your refresh timing. When you are finished, select **Set**. You can also close the timer without saving your selections by selecting **Close**.

3. Set multiple daily refreshes by selecting **Add another time**.

   > [!div class="mx-imgBorder"] 
   > ![](media/system-data-refresh-add-another-time.png "System data refresh add another time")

4. To discard any of your saved timings, select the boxes shown here.

   > [!div class="mx-imgBorder"] 
   > ![](media/system-data-refresh-discard-time.png "System data refresh discard time")

**To schedule a weekly refresh:**

1. Check the boxes for the days on which you want to execute a refresh.
  
  > [!div class="mx-imgBorder"] 
  > ![](media/system-data-refresh-weekly-time.png "System data refresh weekly time")

2. Follow the steps for scheduling a daily refresh to complete the weekly refresh setting.

3. **Save** your changes.

  > [!div class="mx-imgBorder"] 
  > ![](media/system-data-refresh-save.png "System data refresh save")

## About tab
<!--note from editor:  Introduce the screen shot below, or delete it?  -->

> [!div class="mx-imgBorder"] 
> ![](media/system-data-about-tab.png "System data About tab")

Several options are available on this page, as shown in the following example. These options can serve important business requirements, such as using Customer Insights from different regions or distinguishing between multiple work instances.

> [!div class="mx-imgBorder"] 
> ![](media/settings.png "Settings")

- **Display name**: Determine how your user name will be shown.
- **Instance name**: Give your work instances identifiable names. This is recommended if you have more than one instance.
- **Region**: Determine your organization's region.

## General tab

Currently, only one option, **Language**, is available to you on the **General** tab. The languages we support show up in this menu. Don't forget to **Save** your selection. 

> [!div class="mx-imgBorder"] 
> ![](media/system-tabs-general.png "General tab")
