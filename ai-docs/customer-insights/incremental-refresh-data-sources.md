---
title: "Incremental refresh for ingested large data sources in Customer Insights | Microsoft Docs"
description: "Refresh new and updated data for large data sources in Dynamics 365 Customer Insights."
ms.date: 02/05/2020
ms.reviewer: adkuppa
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Incremental refresh for large data sources

Refreshing new and updated data for data sources in Customer Insights provides the following advantages:

- **Faster refreshes** - Only data that has changed gets refreshed. For example, only from the past five days of a historical dataset.
- **Increased reliability** - Reduced necessity to maintain long-running connections to volatile source systems reduces the risk of connection issues.
- **Reduced resource consumption** - Less data to refresh reduces the consumption of computing resources.
