---
title: "Advanced Guide | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/31/2018
ms.reviewer: ""
ms.service: "crm-online"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# Advanced Guide

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

## Ingest
In this section we will explain how to bring data from many of your sources: From CRM systems, to transactional and survey data, to clickstream, social and other data you might have. Connecting all your data sources and completing the Map, Match and Merge phases described below, will enable you to unlock one of the unique promises of the product - consolidating and reconciling data on your customers from multiple sources that once were disperate and conflicting. 

o	Connectors (sources that are not supported by the CDM template)
o	Go deep on .csv files



## Massaging the data
Content.

### Map
Once ingested your data, you are ready to unlock the unique identity-resolution features that Dynamics AI for Customer Insights offers.
In the flow below, you can get a sense for the different relations that exist between your ingested data sources. In Dynamics AI for Customer Insights, those sources are called *Customer Entities*. Clicking the **Map** tile at the bottom of the screen will take you to the first stage in the data configuration process.

(add configuration screen)

The main goal behind the Map screen below is to go customer entity by customer entity and identify for each of them the columns upon which you want to merge the data as part of the later Match and Merge stages. In Dynamics AI for Customer Insights these columns are also called *attributes*. 

(add Map screen)

A table will appear upon clicking each of the customer entities on the left. Now we will explore each of this table's columns, going left to right:
- Primary Key: For executing the identity-resoultion process it's mandatory to **select one column as a unique key** for each of the customer entities. For example..
- Match: Also required selection. Here you will select **all** the columns which you will want to consider as you match data from multiple sources. For example, if you know you have 
- Entity Type
- Normalize

In addition, you have three additional possibilities in the Map screen:
- Add customer entity
- Add attributes to existing customer entity
- Lastly, you have the possiblity to search


### Match
Content.

### Merge
Content.

## Enrichment
due to OOB rules automatically happens but we can link it to the chosen category and mention that the data was enriched with info on preferred brands, interests, etc

## Insights
top paying/engaged/etc customers, KPIs, other details

## Segmentation
o	Work with operators to produce segments (both static and dynamic segments)
o	Act (export segments)

## Extensibilities
Content.

### APIs
Content.

### Power BI
Content.

### Custom apps
Content.

### PowerApps and Flow
Content.

### Other connectors
Content.

## Administration
Content.
