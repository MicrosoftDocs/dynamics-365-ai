---
title: "Service limits in Dynamics 365 Customer Service Insights"
description: "Understand limits and restrictions within the Dynamics 365 Customer Service Insights product."
keywords: ""
ms.date: 10/22/2020
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid:
author: lalexms
ms.author: laalexan
manager: shujoshi
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Service limits in the embedded Dynamics 365 Customer Service Insights

This article describes the built-in limits to the Customer Service Insights service for the embedded version of insights in Customer Service Hub and Customer Service workspace. These limits are designed to ensure the reliability and stability of the service. Any requests for changes can be made through the [Ideas forum](https://go.microsoft.com/fwlink/?linkid=2024757). 
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Cases | 24-month data retention limit. |  |
| Analytics reports | None currently | No limits on number of interactions or drill-throughs within reports. |
| Topics | Three or more related cases for model | Topics are generated from the 100k+ cases. |
| Case suggestions | 30 cases |  |
| Conversation suggestions | 150 conversations | |
| Data refresh | Once every 24 hours | Data refresh occurs automatically each day, starting at midnight UTC. The time when the refresh completes is not guaranteed. For more information, see {Information you need to know about Customer Service analytics reports](https://docs.microsoft.com/dynamics365/customer-service/customer-service-analytics-insights-csh#information-you-need-to-know-about-customer-service-analytics-reports). |
