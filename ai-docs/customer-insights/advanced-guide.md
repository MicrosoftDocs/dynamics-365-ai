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
- ***I am new to the Advanced Mode BUT I did explore the Quick Start documentation*** -> In that case you may want to skip the following sections: *Search and Browse Customer, Profile, Enrichment, Segmentation, and Administration* as these are the same as for *Quick Start*.   
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

## Customers sections
**After completing the Data Manager sections**, you are ready to start benefiting from the various insights you have just unlocked on your customers. The *Profile* and *Segmentation* Customers sections are used for this purpose as well as the *Home* section that will be covered later.

Which of these three sections should you start with? That depends on your goal:
- To get a high-level view of the unique aspects of your customer base as a whole and the latest changes in those aspects, start with the *Home* page, and continue with the *Segmentation* and *Profile* pages (in that order).
- To start with more targeted insights – insights around specific segments of your customer base, start with the *Segmentation* page or the *Enriched Data* page. 
- To understand specific customer aspects and trends, start with the *Profile* page.
- To analyze your top paying, engaged, or active customers, start with the *Profile* page.

## Customers: Profile
This page serves as the best source of insights around each of your customers. 
- The top row lists some of your **Top Paying Customers**.
- The second row present some of your **Most Engaged Customers**. 
- The third row show some of your customers that have the **Most Active Cases**.
- The last row includes a sample of your total customer base .

Each of your customers is represented by a **Customer Card** tile. This card includes:
- The customer's **name, city, gender, marital status and job title** - all taken from the customer's account profile.  
- The Customer's **contact details** including phone number and email address. Those are clickable and will take you to the chosen method of communication.
- The customer's **engagement score:** How engaged is the specific customer compared to other customers? Dynamics 365 AI for Customer Insights uses one of the standard methodologies for calculating engagement score. As part of this methodology, all the customer activities are taken into consideration, weighted according to their types, recencies and frequencies, and normalized on a 1-100 scale. 
- The customer's **lifetime spend:** How much has the customer spent over the course of their engagement with the business. Customer lifetime spend is one of the most comprehensive and actonable indicators of a business health and it combines both sales and deals in process.
- The number of **active cases** and **active segments** for that customer (see Segmentation for an explanation of active segments).  

> [!div class="mx-imgBorder"] 
> ![](media/customer-profiles75.png "Generated customer profiles")

Select **See all** to see more customers sorted by the profile type. In this example, **Top paying** is the profile type.

> [!div class="mx-imgBorder"] 
> ![](media/view-more-customers.png "View more customers")

You can use the customer profiles page to filter and sort the profiles.

> [!div class="mx-imgBorder"] 
> ![](media/filter-sort.png "Filter and sort customer profiles")

What's in the sort list depends on the category you selected earlier and the profile type. 

> [!div class="mx-imgBorder"] 
> ![](media/sort-list.png "Sort list")

Upon clicking a specific customer tile, you will get to the **Power BI report** for that customer which is explored below.

## Customer's Power BI report
This report encapsulates everything you need to know about the specific customer you selected on the *Profile* page. It includes four major parts: The Customer Card, selected customer KPIs, top interests and brands for customers that are like this customer, and this customer's activities. 
- **Customer Card:** This card is the same card that appears for that customer on the *Profile* page that was described earlier.
- **Customer KPIs**: The most insightful key performance indicators (KPIs) across the four customer journey phases:
  - **Awereness KPIs:**
      - sdf
      - sdf
  - **Engagement KPIs:**
      - Engagement score
      - sdf
  - **Fulfillement KPIs:** 
      - Sales
      - Sales in Process
      - Lifetime spend 
  - **Service KPIs:**
      - Number of active cases
      - dsfd

[add power BI report page once finalized!]

- **Top interests and brands**: Top interests and brands were explained in the Enrichment section. **Note**: while the *Home* page shows the top **three** interests and brands of your **aggregated customer base**, the customer's Power BI report shows the top **ten** interests and brands of those customer profiles that are like this specific customer's profile. 

[add power BI report page once finalized!]

- **Customer's activities**: From phone calls, to store visits, to online behavior activities, to many other activities, AI for Customer Insights enables you to capture them all in a way that is meaningful for your business. The part highlighted in blue below includes activities organized by types while the part highlighted in red below includes the same activities organized across the customer's activities journey with corresponding dates and activity durations. 

[add power BI report page once finalized!]

## Customers: Segments
We will explore two ways to create segments. We will also show how to best explore your customer segments.

### Creating segments from the segment page
Within the segments page, select **Add Segment** as shown below to start the segment creation process. You can choose either to create a  ***Static segment***, to create a ***Dynamic segment***, or to go to the *Profile* page and create a segment through the filter tab (explained later):

[]


***Dynamic segments*** change with time as data updates, while ***Static segments*** are fixed. An example for a case that fits Static segment might be exploring the properties of a specific group of customers (for example from a specific location), properties that are not expected to change with time. Segments that are automatically updated with time. A case that fits Dynamic segments is for example tracking the impact of a marketing/sales/service activity on a specific group of customers with time (tracking the change/lift in those KPIs).

- **Segment creation process**:
Once you choose **Add Dynamic Segment** or **Add Static Segment** you go to the **Segment Creation** page:

[divS1]

   - **We start by defining the segment's properties**: We will give our segment a name and description, choose the audience of this segment (in the example below two types are shown: Contacts and Accounts), click the first slider (highlighted in blue below) if we wish to change from Static segment to Dynamic segment or vice versa, and click the second slider (highlighted in red below) to activate our segment (otherwise it will not incorporate new information on our customers as our data is refreshed). 
     
     [divS2]
     
   - **In step two, we will start creating our first filter**. Use the "filter" bar to select an entity. Once we selected an entity type, we need to choose the specific attributes we want to group by our customers. Note that attributes can have one of three value types: A numerical, a string, or a date. In the example below, an attribute with a numerical value is used as a filter:
     
     [divS3]
     
   - **In step three, which is optional, we will add two rules to our filter**. Two roles are available on the entity level: 
     ***AND*** and ***OR***. In the example below, we added to our first role two additional roles. The middle row demonstrates the 
     creation of an "AND" role (this time with a string attribute), while the lower row demonstrates an "OR" role (created for a time 
     attribute):
     
     [divS4]
     
   - **In step four, we will show how to combine multiple filters that are created for multiple entities**. Upon clicking "Add Group" 
     button, three options will show up: ***Union***, ***Intersect*** and ***Exclude***. Clicking each of these options will result in 
     the creation of a new filter for a new entity and the consolidation of this new filter with the filter we created in steps 2-3. Choosing ***Union*** will dictate that the new segment will be fully added to the older segment - no data will be excluded:
       
     [divS5]

       - Choosing ***Intersect*** will dictate that the new segment will be combined with the older segment but if there are missing values among one of the segments, those values will be excluded.

       - Lastly, choosing ***Exclude*** will dictate that the new segment will be combined with the older segment but if there are missing values among one of the segments, those values' columns will be excluded including all their values (both missing and existing values).

### Creating segments from the Profile page
This can be quickly done by setting filtering selections as described in the *Profile* page section and saving those definitions as a segment:

[]

### Exploring segments from the segments screen
Here you can view all your segments as well as suggested segments. These are the page components:
- **Your saved Segments:** Dynamic Segments appear to the left and Static Segments appear to the right. Each segment is represented by a tile that includes the segment name, segment description, last date of data refresh, trend (if exist), the possibility to refresh the data for that segment (as highlighted in blue below), and several other possibilities that can be accessed via  <b>...</b> as highlighted in red below:

[]

Those other options include:
    - Editing this particular segment
    - Viewing it's members
    - Exporting the segment to a .csv file
    - Turning the segment to inactive/active (depends on it's current state)
    - Deleting the segment
    
- **Recommended segments**: Those appear at the lower part of the page as shown below. Those are suggestions that are curated based on your specific customers base. Clicking *Add Segment* in each of the tiles will enable you to build segments for that specific suggestion

[]

### Exploring a particular segment from the segment Page
Once you selected a segment within the *Segments page*, you will get to this page that consolidates everything around that particular segment. As shown below, the upper part includes a trend graph with the possibility to adjust the trend time scope (30 last days, 60 last days, etc.) with the button at the upper-right corner of the tile:

[]

The lower part includes a table with all your segment members properties. Those include: 
- Members Names
- Members Addresses
- Members Job Titles
- Members Telephone Numbers
- Members Cities
- Members States
- Members Locations

### Acting upon the data: Exporting a segment
Exporting a segment to .csv file is possible either through the *Segments page* by selecting <b>...</b> within a specific segment's tile, or by entering the specific segment page and selecting **Export** at the top-right corner of the page as shown here:

[]

Once exported, you can expect to find all the information on that particular segment within the .csv file. An example is shown below:

[]

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-page.png "Segmentation page")

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

