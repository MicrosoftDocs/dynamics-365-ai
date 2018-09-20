---
title: "Quick Start: Dynamics 365 AI for Customer Insights | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/1/2018
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
# Quick Start: Dynamics 365 AI for Customer Insights 

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

Dynamics 365 AI for Customer Insights is a cloud-based SaaS service that enables organizations of all sizes to bring together data from multiple sources and generate knowledge and insights to build a holistic 360° view of their customers. AI for Customer Insights delivers the ability to connect to transactional data sources and model profiles of customers and their interactions. It enables organizations to generate unique insights about their customers which they can tune to clear actions from day one. Customer Insights transforms profiles, interactions, and KPIs into rich visuals that you can customize and organize to focus on what matters to you.

Use this guide to get a quick introduction to the basic features of AI for Customer Insights and come away equipped to use this tool with your data to create actionable insights.

## Select a business category
Once you've installed AI for Customer Insights, the first thing you do is select a business category that most closely matches your industry.

> [!div class="mx-imgBorder"] 
> ![](media/choose-business-category720.png "Select a business category")

Select **More categories** to choose from more industries or business functions. 

> [!div class="mx-imgBorder"] 
> ![](media/more-categories.png "More categories")

Once you select a category, the Home page appears with insights built from sample data.

> [!div class="mx-imgBorder"] 
> ![](media/customers-dashboard780.png "Insights based on sample data for selected category")

## About sample data
Once you've selected a business category, the Home page opens populated with sample data. Insights are built from the sample data automatically. You can explore these insights to get an idea of what AI for Customer Insights can provide when you bring in your data.

If you want to right away bring in your company's data, under **Data Manager**, select **Sources** from the left-side menu.

Then, select a data source. 

> [!div class="mx-imgBorder"] 
> ![](media/choose-data-source75.png "Choose a data source")

Your data will be brought in to AI for Customer Insights and the sample data will be removed. 

If you keep the sample data for now, this topic will walk you through the getting started experience with that data.

## Home page

Based on your ingested data - or, in this case, our sample data - you'll see automatically configured insights into your company's data.

> [!div class="mx-imgBorder"] 
> ![](media/customers-dashboard-3rows.png "Customer dashboard")

### Latest insights
Description of latest insights...

### Top segments
On your Home page, you'll see top segments - segments with the most members and [need content].

Segmentation is the process of slicing and dicing your data by attributes that matter most to you like last purchase date and customer engagement score.

> [!div class="mx-imgBorder"] 
> ![](media/segmenting.png "Segmenting")

For example, you want to know which of your customers are most likely to make another purchase so you can target some ads. 

> [!div class="mx-imgBorder"] 
> ![](media/repurchase-segment.png "Repurchasing segment")

Select the <b>...</b> on a segment tile or open a segment and select **Edit** to see the details.

> [!div class="mx-imgBorder"] 
> ![](media/repurchase-segment-details.png "Repurchasing segment details")

In this example, the segment finds customers who haven't made a purchase in two years and have a high engagement score.

### Data completeness scorecard
Description of data completeness scorecard...


**Awareness**: content

**Engagement**: content

**Fulfillment**: content

**Support**: content

Select a scorecard to see details on the entities used.

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities.png "Scorecard entities")

|Item  |Description  |
|---------|---------|
|**Name**     |The names of your data entities. Those may range from Account to Activity to many other categories. Moreover, note that if there is a warning sign next to one of the entities names, it implies that the data for that entity didn't load successfully.|
|**Last Updated**    |When this entity's data was last updated.         |
|**Lifecycle Phase**    |A typical customer journey goes from Awereness, to Engagement, to Fulfillement (or Conversion), to Service (or Support) , to Advocacy. Within this column each entity is mapped to a specific phase within this journey so your future ability to act upon the data becomes more targeted and ROI-optimized.         |
|**Type**     |The types of your data entities. In some cases, this will be the same as your entity name.    |

## Customers
The Customers section contains information about your customers organized by Profiles and Segments.

### Profiles
Once you've connected to a data source, AI for Customer Insights creates some customer profiles and categories based on your industry type. 

> [!div class="mx-imgBorder"] 
> ![](media/customer-profiles75.png "Generated customer profiles")

Select **See all** to see more customers sorted by the profile type. In this example, **Lifetime spend** is the profile type.

> [!div class="mx-imgBorder"] 
> ![](media/view-more-customers.png "View more customers")

You can use the customer profiles page to filter and sort the profiles.

> [!div class="mx-imgBorder"] 
> ![](media/filter-sort.png "Filter and sort customer profiles")

What's in the sort list depends on the business category you selected and the profile type. 

> [!div class="mx-imgBorder"] 
> ![](media/sort-list.png "Sort list")

### Segments
Content

There are two types of segments:

- **Static**: A static collection of profile data not automatically refreshed.
- **Dynamic**: A collection of profile data automatically refreshed.


**Recommended segments based on your customers**: content

#### Add segment
[divS1]

   - **We start by defining the segment's properties**: We will give our segment a name and description, choose whether it's a segment  
     that is created for accounts (---) or contacts (---), and ensure to leave the Dynamic (blue) switch in "off" state since it is a 
     static segment: 
     
     [divS2]
     
   - **In step two, we will start creating our first filter**. Upon clicking the "filter" bar an entity can be selected. Once we 
     selected an entity type, we need to choose the specific attributes we want to group by our customers. Note that attributes can have      one of three value types: A numerical, a string or a date. In the example below, an attribute with a numerical value is used as a 
     filter:
     
     [divS3]
     
   - **In step three, which is optional, we will add two rules to our filter**. Two roles are available on the entity level: 
     ***AND*** and ***OR***. In the example below, we added to our first role two additional roles. The middle row demonstrates the 
     creation of an "AND" role (this time with a string attribute), while the lower row demonstrates an "OR" role (created for a time 
     attribute):
     
     [divS4]
     
   - **In step four, we will show how to combine multiple filters that are created for multiple entities**. Upon clicking "Add Group" 
     botton, three options will show up: ***Union***, ***Intersect*** and ***Exclude***. Clicking each of these options will result in 
     the creation of a new filter for a new entity and the consolidation of this new filter with the filter we created in steps 2-3.            - Choosing ***Union*** will dictate that the new segment will be fully added to the older segment - no data will be excluded
       
     [divS5]

## Data Manager
Data management settings are considered advanced settings and covered in the [Advanced Mode Manual](advanced-guide.md).

