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

Segmentation is the process of slicing and dicing your data by attributes that are of interest to you like last purchase date and customer engagement score.

> [!div class="mx-imgBorder"] 
> ![](media/segmenting.png "Segmenting")

For example, you want to know which of your customers are most likely to make another purchase so you can target some ads. 

> [!div class="mx-imgBorder"] 
> ![](media/repurchase-segment.png "Repurchasing segment")

Select <b>...</b> on a segment tile or open a segment and select **Edit** to see the details.

> [!div class="mx-imgBorder"] 
> ![](media/repurchase-segment-details.png "Segment details")

In this example, the segment finds customers who haven't made a purchase in two years and have a high engagement score.

### Data completeness scorecard
Dynamics 365 AI for Customer Insights equip you with a range of insights across the customer lifetime journey. However, how confident you can be in regard to these insights? By viewing the Data Completeness Scorecard you can get a sense for the phases for which you have wide entity representation versus the phases for which you should successfully incorporate more data and entities. Going left to right, you can view how complete is your data for the Awereness, Engagement, Buying and Service stages.

For each of these tiles, green represents good entity coverage, yellow represents medium entity coverage, and red represents poor entity coverage.

**Awareness**: need content

**Engagement**: need content

**Fulfillment**: need content

**Support**: need content

Select a scorecard to see details on the entities used. Entities are [need content]

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities.png "Scorecard entities")

|Item  |Description  |
|---------|---------|
|**Name**     |The names of your data entities. Those may range from Account to Activity to many other categories. Moreover, note that if there is a warning sign next to one of the entities names, it implies that the data for that entity didn't load successfully.|
|**Last Updated**    |When this entity's data was last updated.         |
|**Lifecycle Phase**    |A typical customer journey goes from Awareness, to Engagement, to Fulfillement (or Conversion), to Service (or Support) , to Advocacy. Within this column each entity is mapped to a specific phase within this journey so your future ability to act upon the data becomes more targeted and ROI-optimized.         |
|**Type**     |The types of your data entities. In some cases, this will be the same as your entity name.    |

## Customers
The Customers section contains information about your customers organized by Profiles and Segments.

### Profiles
Once you've connected to a data source, AI for Customer Insights creates some customer profiles and categories based on your industry type. Under **Customers**, select **Profiles**.

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
You can create segments of your data to filter on certain elements such as a time range and customer satisfaction to create focused, actionable steps.

There are two types of segments:

- **Static**: A static collection of profile data not automatically refreshed. Example use case: exploring the properties of a specific group of customers, from a specific location - properties that are not expected to change with time. 
- **Dynamic**: A collection of profile data automatically refreshed. Example use case: tracking the impact of a marketing/sales/service activity on a specific group of customers over time.

> [!div class="mx-imgBorder"] 
> ![](media/customer-segments.png "Customer segments")

Based on your data and industry type, you can see a list of segments AI for Customer Insights has created for you.

**Recommended segments based on your customers**: need content

#### Edit a segment
To edit, export, view members, and more for a segment, select <b>...</b> in the segment.

> [!div class="mx-imgBorder"] 
> ![](media/segment-menu.png "Segment menu")

Here you can modify the criteria used to segment the data.

> [!div class="mx-imgBorder"] 
> ![](media/repurchase-segment-details.png "Segment details")

[need content] To add a group select **Add Group**.

#### Add a segment

To add a segment, select **Add Segment**.

> [!div class="mx-imgBorder"] 
> ![](media/add-segment.png "Add segment")

## Data Manager

### Sources

To bring in your company's data, select **Sources** then select a data source. 

> [!div class="mx-imgBorder"] 
> ![](media/choose-data-source75.png "Choose a data source")

Your data will be brought in to AI for Customer Insights and the sample data will be removed. 

### Entities
Entities are [need content]

After ingesting the data, you can quickly evaluate how complete and useful it is using the Entities screen. If you suspect that your ingested data is not complete or useful enough, you can import more data using **Import Data**. You can also export the entities table as a csv file by selecting the **Export Data**.

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities.png "Entities")

Select an entity to see information about it.

> [!div class="mx-imgBorder"] 
> ![](media/customer-entity-details.png "Customer entity")

|Item  |Description  |
|---------|---------|
|**Fields**     |need content |
|**Keys**    |need content         |
|**Relationships**    |need content |
|**Data**     |need content  |

## Configuration, Relationships
Other data management settings  will be covered in future documentation.

## Admin

### Permissions
Use the forms in the **Permissions** section to add or remove role permissions to AI for Customer Insights.

**Roles**

|Role  |Description  |
|---------|---------|
|Contributor    |need content |
|Reader  |need content        |
|Admin   |need content |
