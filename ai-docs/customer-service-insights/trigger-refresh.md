---
title: "Trigger a refresh of your Customer Service Insights data"
description: "Learn how to trigger a refresh of your Customer Service Insights data."
keywords: ""
ms\.date: 4/1/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Trigger a refresh of your Customer Service Insights data

[!INCLUDE [public-preview](../includes/public-preview.md)]

Customer Service Insights automatically refreshes the data displayed on dashboards daily. However, you may want dashboards to display data that is more current than the data from the last automatic refresh.

If you want to update the dashboards to use current data, you can trigger a refresh on demand without waiting for next daily refresh. Customer Service Insights gives you the option of refreshing your workspace when you make any of following changes:

* Update data mapping settings
* Change case title cleansing settings
* Change topic granularity settings
* Rename a topic

For example, when you rename a topic on the Topics dashboard, Customer Service Insights displays a prompt at the top of the dashboard that gives you an opportunity to refresh your workspace. To refresh the workspace, select **Refresh**.

   > ![Refresh workspace](media/refresh-workspace.png)

**Note:**  There is a limit of 10 on-demand refreshes per day per workspace.

For more information on data mapping settings, see [Map your data to custom entities and fields](map-data.md).

For more information on case title cleansing settings, see [Improve data quality by cleansing support case titles](settings.md).

For more information on topic granularity settings, see [Set the scope of how Customer Service Insights generates customer service topics](granularity.md).

For more information on renaming a topic, see [Renaming a topic](dashboard-topics.md#renaming-a-topic).