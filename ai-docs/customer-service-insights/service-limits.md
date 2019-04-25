---
title: "Service limits in Dynamics 365 Customer Service Insights"
description: "Understand limits and restrictions within the Dynamics 365 Customer Service Insights product."
keywords: ""
ms.date: 4/25/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: tpalmer
ms.author: tpalmer
manager: shellyha
---

# Service limits in Dynamics 365 Customer Service Insights

This article describes the built-in limits to the Customer Service Insights service, which are designed to ensure the reliability and stability of the service. Any requests for changes can be made through the [Ideas forum](https://go.microsoft.com/fwlink/?linkid=2024757). 
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Data import | Cases created in the last 60 days, or 1 million cases   | The number of cases that can be imported is determined by your organization's licensing. See [Licensing and case capacity considerations](licensing-case-capacity.md) for details. <br> <br> Cases created on the same day a workspace is created will be imported through the daily refresh on the following day. |
| Automatic data refresh | Once every 24 hours | Automatic data refresh occurs automatically, starting at midnight UTC. The time when the refresh completes is not guaranteed. |
| Manual data refresh | On demand data refresh is allowed up to 10 times per day | After the limit is reached, you need to wait for the automatic refresh to occur for the manual refresh limit to reset. For more information about the manual data refresh, see [Trigger a refresh of your Customer Service Insights data](trigger-refresh.md).  |
| Data location | Data is located in the same region as the Dynamics 365 environment the data is connected to.     | Geographical location of data occurs automatically and cannot be controlled by users at this time. |
| Dashboard interactions | None | There are no limits on the number of interactions allowed on dashboards, such as cross filtering or drill-through |
| Connecting to a Dynamics 365 environment | One workspace per Dynamics 365 environment per user | A Dynamics 365 environment cannot be connected with multiple workspaces at the same time by the same user. If a workspace is created and then deleted, it can be connected  again. <br> <br> In addition, a single workspace cannot be connected to more than one Dynamics 365 environment. |
| Topics generated from cases | Topics are only be generated from cases when there are at least three related cases| Because topics are automatically created based on similar customer service cases, the system needs a minimum number of cases to create a topic. <br> <br> In order for topics to be meaningful, we recommend having at least 1000 cases.|
