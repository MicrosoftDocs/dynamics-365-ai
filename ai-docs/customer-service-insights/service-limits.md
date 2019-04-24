---
title: "Limits across Customer Service Insights"
description: "Understand limits and restrictions within the Customer Service Insights product."
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

# Limits across Customer Service Insights

[!INCLUDE [public-preview](../includes/public-preview.md)]

Dynamics 365 Customer Service Insights comes with built-in limits to ensure the reliability and stability of the service. This document describes those limits, any requests for changes can be done through the [Ideas forum](https://go.microsoft.com/fwlink/?linkid=2024757). 
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Data Import | Cases created in the last 60 days <br> or <br> 1 million cases   <br> (which ever limit is hit first)| The number of cases imported may affected by licensing, see Licensing Overview for more details. <br> The cases created in the same day when a workspace is created will be imported through daily refresh in the next day. i.e. cases created “today”   are not imported. |
| Automatic Data Refresh | Once every 24hrs | This happens automatically and is kicked off at midnight UTC, but is not   guaranteed when to complete. |
| Manual Data Refresh | On demand up to 10 times per day | Once the limit is hit, wait for the automatic refresh to occur and the limit will be reset. |
| Data geolocation | Data will be geolocated in the same region as the Dynamics 365 CDS environment it is connected to.     | This happens automatically and cannot be controlled by users at this time. |
| Dashboard interactions | None | There are no limits on the number of interactions (cross filtering, drill through etc.) on the dashboards |
| Connecting to a Dynamics 365 CDS environment | One workspace per Dynamics environment per user | A Dynamics environment cannot be connected with multiple workspaces at the same time by the same user. If a workspace was created and then deleted, it can be connected to again. Also a single workspace cannot be connected to more than one Dynamics environment. |
| Topics generated from cases | Topics will only be generated from cases if there are minimum of 3 related # cases| As topics are automatically created based on similar customer service cases, the system needs a minimum number of cases to create a topic. In order for topics to be meaningful we recommend having at least 1000 cases.|
