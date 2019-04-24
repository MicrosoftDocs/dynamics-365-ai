---
title: "Service limits in Dynamics 365 Customer Service Insights"
description: "Understand limits and restrictions within the Dynamics 365 Customer Service Insights product."
keywords: ""
ms\.date: 4/24/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: tpalmer
ms.author: tpalmer
manager: shellyha
---

# Service limits in Dynamics 365 Customer Service Insights

This article describes the built-in limits to the Customer Service Insights service, which are designed to ensure reliability and stability . This document describes those limits, any requests for changes can be done through the [Ideas forum](https://go.microsoft.com/fwlink/?linkid=2024757). 
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Data Import | Cases created in the last 60 days <br> or <br> 1 million cases   | The number of cases imported is affected by licensing. See [Licensing and capacity overview](licensing-overview.md) for more details. <br> The cases created in the same day when a workspace is created will be imported through the daily refresh on the following day. |
| Automatic Data Refresh | Once every 24 hours | This happens automatically and starts at midnight UTC, but is not guaranteed when to complete. |
| Manual Data Refresh | On demand up to 10 times per day | Once the limit is hit, wait for the automatic refresh to occur and the limit will be reset. |
| Data location | Data will be located in the same region as the Dynamics 365 CDS environment it is connected to.     | This happens automatically and cannot be controlled by users at this time. |
| Dashboard interactions | None | There are no limits on the number of interactions (cross filtering, drill through etc.) on the dashboards |
| Connecting to a Dynamics 365 CDS environment | One workspace per Dynamics environment per user | A Dynamics environment cannot be connected with multiple workspaces at the same time by the same user. If a workspace was created and then deleted, it can be connected to again. Also a single workspace cannot be connected to more than one Dynamics environment. |
| Topics generated from cases | Topics will only be generated from cases if there are at least 3 related cases| As topics are automatically created based on similar customer service cases, the system needs a minimum number of cases to create a topic. In order for topics to be meaningful we recommend having at least 1000 cases.|
