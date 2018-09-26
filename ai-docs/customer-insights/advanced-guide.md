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

## How to use the Advanced Guide
All product sections are accessed through their corresponding tab names in the left-side menu of the app as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/customer-dashboard-full.png "Customer dashboard")

In order to best utilize this manual for your specific needs, you should identify your situation:
- ***I am new to the product AND I didn't go through the Quick start documentation*** -> In that case you may want to explore the manual from start to end. As shown below, product sections are represented by tabs on the left-side menu. This guide's flow reflects the order by which you should work with the product: **Completing the *Data Manager* sections and only then exploring *Segments, Profile and Homepage*** sections.
- ***I am new to the Advanced guide BUT I did explore the Quick Start documentation*** -> In that case you may want to skip the following sections: *Search and Browse Customer, Profile, Enrichment, Segmentation, and Administration* as these are the same as for *Quick Start*.   
- ***I am already using the product but incurring a specific issue*** -> In that case you may want to identify what product section this issue relates to and read on this particular section. 

**Note**: you can return to documentation on any of the product pages by selecting the question mark:

> [!div class="mx-imgBorder"] 
> ![](media/help-link.png "Help link")

<!--
## Onboarding (for Administrators)
Currently missing (9/17)
-->

## Choose a business category
Just as for Quick Start mode, the first thing you do is select a business category that matches your industry:

> [!div class="mx-imgBorder"] 
> ![](media/choose-business-category720.png "Select a business category")

Select **More categories** to choose from more industries and business functions:

> [!div class="mx-imgBorder"] 
> ![](media/more-categories.png "More categories")

## Bring in your data
Once you've selected a business category, sample data is loaded with pre-configured profiles and segments for you to explore.

To bring in your own data, under **Data Manager** select **Sources** and choose a data source. Proceed through the pages to load your data. Once loaded, the sample data will be removed.

> [!div class="mx-imgBorder"] 
> ![](media/choose-data-source75.png "Choose a data source")

## Workflow
If you never used Dynamics 365 AI for Customer Insights before, this is the workflow you can expect to go through:

> [!div class="mx-imgBorder"] 
> ![](media/workflow720.png "Workflow phases")

## Home page
A range of actionable insights were derived during the data ingestion, configuration and enrichment processes and the *Home Page* is where you will find a consolidation of those insights in a way that is tailored around your specific needs. It consists of four major parts as explained below.

> [!div class="mx-imgBorder"] 
> ![](media/customers-dashboard780.png "Home page")

-	**Insights around your overall customer base**: Exploring left to right, those insights include: 
      - **Top Selling Products**: Shows your three top selling products by monetary value or by unit volume. 
      - **Median Lifetime Spend (ML-powered)**: Whether it’s marketing, sales, support or other function, customer lifetime spend is one of the most comprehensive and actionable indicators of your business viability as it captures the customer value across all it’s journey phases. **Possible Usage:** Getting a sense for your overall business health before zooming into major effectors through segmentations and other indicators.
      - **Highest Interests and most preferred Brands of your Customer Base**: These insights were explained within the Enrichment section. **Note**: while the power BI report shows the top ten interests and brands for each of your customer profile types, the *Home page* shows the top **three** interests and brands of your **aggregated customer base.**

()

-	**Top segments**: As part of segmentation you were provided both with recommended segments and with the ability to create new segments. Within the *Home page* you can define which of all your segments are your most important segments to track. These will show up as *Top Segments* and automatically update with time so viewing trends is also at your fingertips. 

()

- **Data completeness scorecard**: AI for Customer Insights equips you with a range of insights across the customer lifetime journey. However, how confident you can be in regard to these insights? By viewing the *Data Completeness Scorecard* you can get a sense for the phases for which you have wide entity representation versus the phases for which you should successfully incorporate more data and entities. 
   -Going left to right, you can view how complete is your data for the Awareness, Engagement, Buying and Service stages.   
   -For each of these tiles, *Green* represents good entity coverage, *Yellow* represents medium entity coverage and *Red* represents poor entity coverage. 
   
()

-	**Learn how to use Dymanics 365 AI for customer Insights:** Include four quick-help options that are linked to the user guide:
    - **Getting Start with Dymanics 365 AI for customer Insights**: How to get started with the product? Takes you to the documentation of the Quick Start version of the product.
    - **Dynamics 365 AI for Customer Insights guided learning**: How to use the advanced version of the product? Takes you to this manual 
    - **Tutorial: Dynamics 365 for Customer Insights in a day**: Exemplifies how to use the product as part of a typical work day
    - **Map, Match, Merge and Segment**: Takes you to these specific sections within the user manual as they encapsulate more mandatory configurations than the other product sections


## Extensibilities

### APIs 
**Swagger - in progress**

> [!div class="mx-imgBorder"] 
> ![](media/custom-app.png "Custom app")

### PowerApps and Flow
Show how a user can setup triggers to drive actions (e.g. use Flow to ! mail to account manager when churn score increases by 10+%)
Show how a user can setup triggers on events detected in profile to drive relevant actions (e.g. if a customer tweets a complaint, notify customer service department to reach out and resolve)

> [!div class="mx-imgBorder"] 
> ![](media/powerapps-flow.png "Flow")

