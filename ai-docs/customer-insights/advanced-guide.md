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

The main goal behind the Map screen below is to go one customer entity at a time, and identify the columns upon which you will want to merge your data. In Dynamics AI for Customer Insights these columns are also called *attributes*. 

(add Map screen)

Clicking each of the customer entities tabs on the left will open it's corresponding attributes table. Below we will explore each of this table's columns, going left to right:
- Primary Key: For executing the identity-resoultion process it's mandatory to **select one attribute as a unique key** for each of the customer entities. For example..
- Match: Also required selection. Here you want to select **all** the attributes that might correspond to attributes in other customer entities. examples include customer ID, email address, and many other attributes that you might find in multiple data sources. Moreover, you may want to select attributes even if you expect partial overlap with attributes from other data sources since not-exact matchings will also be available to you as part of the next *Match* stage. 
- Entity Type: Pre-defined categories under which your attributes fall such as email or name. No action is required here.
- Normalize: 

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
