---
title: "Demographic insights in Dynamics 365 Market Insights | Microsoft Docs"
description: "Insights related to the demographics insights type."
ms.date: 09/24/2019
ms.service: dynamics-365-ai
ms.topic: article
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

# Demographic insights

(This topic is pre-release documentation and is subject to change.)

## Overview

Obtaining accurate customer demographic information can be an expensive and time consuming task.

**Gender** and **Age** insights provide a view with the percentage of male and female distributions, as well as age distribution of those who are searching for elements you defined.

![Demographic insight in the Market Insights app](media/insight-details-demographics.png)

## Data and frequency

**Gender** and **Age** distribution will show up right after an element is added. An insight will be delivered when a significant change (a change in share of voice among the gender segments that is more than what has been observed in the past year) is detected.

**Demographic Insights** aggregates data from users who search for related terms on [https://www.bing.com/](https://bing.com) for the topic selected. Each user is assigned to a demographic segment by using Data science models on the user's search query terms and patterns from multiple search sessions.
