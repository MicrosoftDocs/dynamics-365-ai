---
title: "Data science concepts applied to Alerts | Microsoft Docs"
description: "Data science for alerts in Market Insights."
keywords: "data science, alerts, daily digest, email"
ms.date: 04/01/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 8f826a0a-b807-4342-81ba-d4df94496dee
author: m-hartmann
ms.author: mhart
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# How relevancy in determined in alerts

## Choosing news articles

Based on the keywords used in your alert configuration, the system crawls the web for matching news. If a matching article is found, we check if it's a duplicate of another matching article and how relevant the publishing website is. The most relevant articles are sent to you in the alert email.

## Learning from your feedback

In the email digest, every news has a control to **Flag as a irrelevant**. If you select this link, the system learns from your feedback and determine why the article isn't relevant. These learnings are used to increase the relevance of your alerts in the future.

### See also
[Market Insights Alerts overview](alerts-overview.md)    
[Manage your alerts](alerts-management.md)