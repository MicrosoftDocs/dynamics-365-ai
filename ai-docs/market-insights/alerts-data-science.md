---
title: "Data science concepts applied to alerts | Microsoft Docs"
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

(This topic is pre-release documentation and is subject to change.)

## Choosing news articles

Based on the keywords and their related categories used in your alert configuration, the system crawls the web for matching news. If a matching article is found, we check how relevant the publishing website is. We prefer fresher and more up-to-date news. The most relevant articles are sent to you in the alert email. We only select articles that discuss the selected topic significantly while avoiding articles containing only a brief reference to that topic. Additionally, the more people read an article, the more relevant it is.

## Identifying related topics that are trending

The system tries to understand the topic category you are following to ensure you get topics relevant these categories. We further avoid repetition and improve the relevancy of related topics that are trending by clustering synonymous topics and focusing on new and breaking topics. Topics are grouped by their change in volume to give further insights how they have evolved in the recent past.

## Learning from your feedback

In the email digest, every news has a control to **Flag as a irrelevant**. If you select this link, the system learns from your feedback and determine why the article isn't relevant. These learnings are used to increase the relevance of your alerts in the future.

### See also
[Market Insights alerts overview](alerts-overview.md)    
[Manage your alerts](alerts-management.md)