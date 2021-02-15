---
title: "Trigger a refresh of your Customer Service Insights data"
description: "Learn how to trigger a refresh of your Customer Service Insights data."
keywords: ""
ms.date: 4/25/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Trigger a refresh of your Customer Service Insights data

Customer Service Insights automatically refreshes the data displayed on dashboards daily. However, you might want dashboards to display data that is more current than the data from the last automatic refresh.

> [!IMPORTANT]
> There is a limit of 10 on-demand refreshes per day per workspace.

If you want to update the dashboards to use current data, you can trigger a refresh on demand without waiting for the next daily refresh. Customer Service Insights gives you the option of refreshing your workspace when you make any of following changes:

* Update data mapping settings
* Change case title cleansing settings
* Change topic granularity settings
* Rename a topic
* Move cases to another topic

For example, when you rename a topic on the Topics page, Customer Service Insights displays a prompt at the top of the dashboard that gives you an opportunity to refresh your workspace. To refresh the workspace, select **Refresh**.

![Refresh workspace](media/refresh-workspace.png)


> [!NOTE]
> If the scheduled daily refresh didn't get the latest data, it's likely due to your sign-in token being expired. This issue will resolve itself as soon as you log back in to Customer Service Insights, and you can use manual refresh to get the latest data.

For more information on data mapping settings, see [Map your data to custom entities and fields](map-data.md).

For more information on case title cleansing settings, see [Improve data quality by cleansing support case titles](settings.md).

For more information on topic granularity settings, see [Set the granularity of how Customer Service Insights generates customer service topics](granularity.md).

For more information on renaming a topic, see [Renaming a topic](topics-page.md#renaming-a-topic).


[!INCLUDE[footer-include](../includes/footer-banner.md)]