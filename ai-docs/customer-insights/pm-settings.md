---
title: "System| MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/21/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
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

The **System** page encapsulates everything that you, as an administrator, needs to have in order to closely monitor the various processes that run behind the scenes of Customer Insights. As shown below, it includes four parts: **Status, Schedule**, **About**, and **General**.

> [!div class="mx-imgBorder"] 
> ![](media/system-menu.png "System menu")

**Note**: We recommend you use the **Schedule tab** to ensure your data sources are updated on regular basis.

## Status tab

> [!div class="mx-imgBorder"] 
> ![](media/system-menu.png "Status tab")

The **Status** tab enables you to track the progress of data ingestion as well as several important product processes. With that, you can ensure the completeness of any major process you define in Customer Insights. This tab includes three tables.

- **Data Sources**: This table lists all the data sources from which you are ingesting your data (left column as shown below). It also presents the status of ingestion (middle column) - whether it didn't start, is in progress, or already completed. Lastly, the date of the last data refresh is specified per data source (right side column).

> [!div class="mx-imgBorder"] 
> ![](media/system-data-sources.png "System data sources")

- **System Processes**: This table lists all the processes that should be executed in Customer Insights as part of a full user journey (left column as shown below). It also presents the status of these processes (middle column) - whether it wasn't configured by the user, was configured by the user but still in progress, or was completed. Lastly, the date of the last data refresh is specified per data source (right side column).

- In addition, you can view the details of each refresh, given data source, or process gone through by selecting that data source or process. 

## Schedule tab

Use the **Schedule** tab to refresh all of your ingested Customer Insights data. You should utilize this tab to schedule the frequency and timing of the refreshes. As data is constantly updated in your data sources, you may want the Customer Insights processes and insights to reflect those changes. The **Schedule** tab enables you do achieve that in an automated way.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-off.png "System data refresh off")

In Customer Insights, the default state for data refresh is **Off**, reflecting no scheduled refreshes. To change it, use the slider at the top of the screen (changing it to  **On** status).

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-on.png "System data refresh on")

The next step is to decide between **Weekly** (default) and **Daily** refresh. 

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-period.png "System data refresh period")

First we will demonstrate the definition of a daily refresh, and then we will continue with the case of a weekly refresh.

First, select the **Time** field.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-time-period.png "System data refresh time period")

In the timer shown above, select the four arrows to set your refresh timing. When finished, select **Set**. You can also close the timer without saving your selections by selecting **Close**.

Set multiple daily refreshes by selecting **Add another time**.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-add-another-time.png "System data refresh add another time")

To discard any of your saved timings, select the check boxes.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-discard-time.png "System data refresh discard time")

To schedule a weekly refresh, check the boxes for the days in which you want to execute your refreshes.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-weekly-time.png "System data refresh weekly time")

Follow the steps specified above for daily refresh setting.

Save your changes.

> [!div class="mx-imgBorder"] 
> ![](media/system-data-refresh-save.png "System data refresh save")

## About tab

> [!div class="mx-imgBorder"] 
> ![](media/system-data-about-tab.png "System data About tab")

In this page, several options are available as shown below. Those options can serve important business requirements such as using Customer Insights from different regions or distinguishing between multiple work instances.

> [!div class="mx-imgBorder"] 
> ![](media/settings.png "Settings")

- **Display Name**: Determine how your user name will be shown.
- **Instance Name**: Give your work instances identifiable names. Recommended if you have more than one instance.
- **Region**: Determine your organization's region.

## General tab

Currently, only one selection is available to you via the **General** tab - **Choosing language**. The languages we support show up in this menu. Don't forget to **Save** your selection. 
