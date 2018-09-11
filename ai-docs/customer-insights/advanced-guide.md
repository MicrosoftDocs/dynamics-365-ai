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

### Introduction to Data Configuration
Once ingested your data, you are ready to unlock the unique data-configuration features that Dynamics AI for Customer Insights offers. In the flow below, you can get a sense for the different relations that exist between your ingested data sets. In Dynamics AI for Customer Insights, those datasets are called **Customer Entities**. Clicking the **Map** tile at the bottom of the screen will take you to the first stage in the data configuration process.

(add "configuration" screen with highlighted Map tile)

### Map
There are two main goals behind the Map screen (shown below):
- Entity selection: Identifying the customer entities which might include overlapping or partially ovelapping data
- Attribute selection: For each customer entity, identifying the columns upon which you will want to merge your data (also called **Attributes**)

(add "Map" screen)

Clicking each of the customer entities tabs on the left will open it's corresponding attributes table. Below we will explore each of this table's columns, going left to right:
- **Primary Key:** For executing the identity-resoultion process it's mandatory to **select one attribute as a unique key** for each of the customer entities. For example, if one of your data sources is a contacts dataset, you may want to assign *customer name* as the unique key for that source, while for a call logs file you may define *phone number* as a unique key.
- **Match:** Also required selection. Here you want to select **all** the attributes that might correspond to attributes in other customer entities. Examples range from customer ID, to email address, to many other attributes that you might find in multiple datasets 
- **Entity Type:** Categories under which your attributes fall such as email or name. Adding a custome entity type is also possible.
- **Normalize:** Optional column. Here you can select whether and how to normalize all the data that you use for the matching prcosess. Several options are available such as removing whitespaces, normalizing digits, removing punctuation, and others. 

In addition, three additional actions are available in the Map screen:
- **Add customer entity:** Available upon clicking the ***Add*** drop-down menu (shown below, left image). Here you can bring additional data sets from your data sources on the basis of which you wish to match your data. 
    - Using the customer entitys panel (shown below, center image), first you want to click on the data source from which you wish to add more customer entities. In the example below, clicking the *Dynamics* datasource opened a list with all the entities for that source. You may also use the search botton to find a specific entity.
    - Next, you want to select the entities that you want to add. In the example below (right image) few entities have been selected.
    - Lastly, you want to save your selection and now these will be added as new tabs to the left of the entity table. 

(add "Map adding dataset" 3 screens - one next to another)

- **Add attributes to an existing customer entity:** Available upon clicking the ***Add*** drop-down menu (left image below). Choosing this option for one of your customer entities will enable you to take more attributes into consideration as part of the matching process. [UX is not ready for selection panel]

(add "Map add customer field" 3 screens - one next to another)

- **Keep unmatched records:** As part of the next stage (match), it is possible that not all of your data entities will be matched. Upon checking this box (shown below), you choose to save all the records (or dataset rows) of your unmatched entities in your master data profile for future use. This option is recommended if.. [(to complete)] 

(add "Map keep unmatched records" screen)


### Match
Once mapping is completed, you are ready to match your mapped entities. Clicking the Match tile in the configuration screen will take you to the Match screen.

(add "configuration" screen with highlighted Match tile)

In the Match screen below, some matches were already automatically identified based on your map pahse selections. However, since there are many ways and orders by which customer entities might be matched, this phase enables you to specify the match logic that best resonates with:
- Your understanding of how your datasources are related to one another
- Your understanding of what sources are most reliable for your mapped attributes.  
Things will become more clear as we go through the matches and roles editing processes.

(add Match screen)

Exploring the Match screen

Editing Roles

Editing Matches

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
