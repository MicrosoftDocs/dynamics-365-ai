---
title: "Frequently asked questions for Dynamics 365 Market Insights | Microsoft Docs"
description: "Find answers to frequently asked questions about Market Insights."
keywords: "FAQ, questions, common issues"
ms.date: 08/20/2019
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

# FAQ for Dynamics 365 Market Insights Preview

(This topic is pre-release documentation and is subject to change.)

Are you new to Market Insights or looking for some help? We've compiled a list of frequently asked questions and provided brief answers to help you get to your information quickly.  

## Where does the data come from?

Market Insights uses billions of data points, mainly from searches which web users performed and browser data. For more information, see [Data sources used in Dynamics 365 Market Insights](about-data.md).

## What does “normalized search volume" mean?

We provide search volume on a scale from 0 to 100 where 100 represents the peak search volume for an element in the given time period. All other data points are relative to this peak search volume. A value of 50 means the element is half as popular from its peak popularity. A value of 0 means that there isn't enough search volume data to provide a normalized value.

## How do you determine what's relevant to me?

TO DO (Pushpraj)

## How does Market Insights use artificial intelligence?

TO DO (Pushpraj)

## What is a spike increase vs. a gradual increase?

A spike represents a significant increase in search volume over a 24-48 hour period. A gradual increase represents a significant increase in search volume over a 28 or 90 day period. Market Insights uses rolling averages to ensure the increases truly represent a rising interest.

## How often do insights get updated?

It depends on the type of insights. Some are updated daily, others less frequently. Please refer to the documentation about the available insights to learn more.

## What is a "verified" company or product?

We maintain a curated set of entities based on the most popular search queries. These entities are well understood by the system and come with enriched information. **Verified** indicates that the selected element is one of our curated entities. Market Insights can provide better and richer insights for verified entities.
