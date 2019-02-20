---
title: "Segmentation| MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/21/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
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
---
# Segments 

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Introduction to Segmentation

> [!div class="mx-imgBorder"] 
> ![](media/segments-allcustomers-status-active.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-group1-define-filter.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-group1-define-filter-settings.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-group1-define-filter-settings2.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-group1-define-filter-settings3.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-group1-define-filter-settings4.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-group1-define-filter-settings5.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-example-entities.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-example-entities2.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-list.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/segments-list2.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/system-tabs.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/system-status-processes.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/system-database-details.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/system-tabs-general.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profiles.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-entities-data-info.png "Text")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-entities-data-info.png "Text")

The *Segments* capability enables you to group your customers into cohorts based on demographic, transactional, or behavioral customer attributes. Using segmentation you can achieve more targeted actions such as promotional campaigns, sales activities, or customer support actions to achieve desired business goals. You can define complex filters around the *Customer Profile* entity and its graph of related entities. Each segment, after processing, outputs a set of customer entity records which you can export and take actions upon.

There are two types of segments:

- **Static**: A segment that is processed only once - either upon the creation or update of any of its filters. Such segments are especially useful for cases when properties are not expected to change over time or that are expected to be used only once. Example use case: Customers who attended an expo event. 
- **Dynamic**: A segment that is processed according to a recurring schedule. These segments are especially useful when customers' attributes change over time. Example use case: Customers who have bought products worth more than $500 in the last 3 months. The current dynamics segment refreshing schedule is every 12 hours.

The example below illustrates the depth of the Customer Insights segmentation capability. Within this complex segmentation scenario, we aim to define a segment for customers who have placed order of more than $500 in last 90 days **and** had an escalated case in last 30 days so they can be followed up with a satisfaction survey. Later, we will learn how to produce such segments. 

<!-- 
{final1:Example of complex segment with multiple groups}

{final2:Insert segment definition diagram created by Nimrod, highlighting Group 1 and Group 2}
-->

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-group1-2.png "Mulitple groups")

- Group 1 uses *Order* as the starting entity in order to find customers who placed an order for more $500 in the last 90 days.
- Group 2 uses *Case* as the starting entity in order to find customers who have an escalated case in the last 30 days.

<!--
> [!div class="mx-imgBorder"] 
> ![](media/segmentation-conceptual.png "System and custom relationships created during configuration")

The example data graph above reflects system and custom relationships created during configuration. The data graph helps dictate the sequence by which segmentation filter criteria are defined within the Segment Editor page.
-->

The two sections below will cover segment creation followed by segment exploration.

## Creating segments from the Segment page

In order to start creating a segment, you can either select **Add Segment** at the top-right corner of the screen (shown in red below), or select **Get Started** (shown in blue below).

<!-- [replace with segments 1]: -->

> [!div class="mx-imgBorder"] 
> ![](media/add-segment-full.png "Add segment")

If you selected **Add Segment** you will also need to select whether you want to create a static segment or a dynamic segment at this point.

Then, the rest of the segment creation process is done in the **Segment Editor** page:

> [!div class="mx-imgBorder"] 
> ![](media/new-dynamic-segment.png "New dynamic segment")

### Step One: Defining the segment's properties

- We will give our segment informative name and description that will help us identify it in the future when we will have multiple segments. 
- Moreover, solely for a dynamic segment, we can also choose to **activate** it at this point through the slider as shown in blue below. **An active (dynamic) segment will automatically incorporate changes** that are made to your data with time while **inactive segment will not incorporate any changes** that are made to your data. 

// update 1
> [!div class="mx-imgBorder"] 
> ![](media/new-dynamic-segment-hilites.png "Change segment type")
   
### Step Two: Creating a first group 

In Customer Insights, **a group is a set of customers.** First we will explain how a group can be defined. If you prefer to view an example, we will provide one right after this explaination.

**Each group's definition involves:**
1. Choosing the entity that includes the specific attribute you wish to segment by. For example, choosing an *Orders* entity since it includes a *Order Value* field by which we want to segment. In order to choose your entity of interest, click the field shown below:

// missing 1

2. Choosing the attribute by which you wish to segment. Our attribute can have one of four value types: A numerical, a string, a date, or a Boolean. In the example below, an attribute with a numerical value is used as a filter.
3. Choosing an *Operator* and a *Value* for the attribute we chose in (2). In the example below an operator *Equal* and value *2* were chosen.

> [!div class="mx-imgBorder"] 
> ![](media/customer-group-numbers.png "Customer group filter")

|Number |Definition  |
|---------|---------|
|1     |Entity          |
|2     |Attribute          |
|3    |Operator         |
|4    |Value         |

Note that one of the segmentation strengths of Customer Insights is the rich variety of operators it supports. Here is a table that summarizes all the operators that are currently supported for the four different value types. It also specifies which operators can be combined to produce complex segmentations.

4. Adding entities that are related to that entity until getting to the Customer Profile entity. That can be done using the **ADD** operator. If not already done, we can define the required relationships between our entities using the **Relationships** page (see the Relationships section for more information). For these additional entities we should choose the *All Records* attribute.

### Example - Group Creation
Let us explore a case in which we wish to segment our customers by a specific clickstream activity attribute. In our example it will be a session ID that is not equal to 1 (since this session was done on an older, outdated website version which is irrelevant for our current targeting efforts).   

**Here the series of steps we should follow:**
1. ClickstreamData: WebsiteDataBase

**Note**: At this point it is recommended to save your first group's definitions as shown below.

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-save-group-definition.png "Save group definition")

### Step Three (optional): Add more conditions to your group 

The following two logical operators can be used for that purpose:

- **AND**: Under this option, both conditions must be met as part of the segmentation process. This option is most useful when you define conditions across different entities (one condition per entity) as shown below.
    
  > [!div class="mx-imgBorder"] 
  > ![](media/segmentation-both-conditions.png "Both conditions met")
    
- **OR**: Under this option, either one of the conditions need to be met as part of the segmentation process. This option is most useful when you define multiple conditions for the same entity as shown below.
    
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-either-condition.png "Either conditions met")

**Note**: At this point it's possible to nest an OR operator under an AND operator but not vice versa.

### Step Four (optional): Combine multiple groups via set operators

Each group produces a specific set of customers. Start by selecting **Add Group**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-group-add-group.png "Customer group add group")

Then three set operators will show up: **Union**, **Intersect**, and **Exclude**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-group-union.png "Customer group add union")
  
Selecting each of these *Set Operators* will enable you to define a new group. At the same time, upon saving each of these will lead to a different result:

- **Union** will unite the new group you have created in Step Four, with the group you have created in Steps Two and Three. Under this option, data that is common to both groups will be maintained, as well as data that is not common to both groups.

- **Intersect** will intersect the two groups. Only data that is common to both groups will be maintained in the unified group.

- **Exclude** will exclude the two groups. Only data that is not common to both groups will be maintained.
   
## Explore segments from the Segments page

// missing 9

Here you can view all your saved segments and perform certain actions.

- Dynamic Segments appear to the left and Static Segments appear to the right.
- Each segment is represented by a tile that includes the segment's name, description, last date of data refresh, and historical trend (if exists). Hover over the trendline to see last week growth in this segment's members count. If you prefer to view all of your segments in a table format, select of the following:

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-static-segment.png "Static segment")

You can also perform certain actions with each segment. First click the following button on the segment's tile:

// missing 10

Then choose one of the following options from the drop down menu:
- Editing the segment.
- Viewing segment's members
- Exporting the segment to either a CSV file, or to a Customer Engagement location.
- Turning the segment to inactive/active (depends on its baseline state).
- Deleting the segment .
- Pin the segment, which will move it to the top of the screen for better accessibility. The pinned segment will show up under **Pinned Segments** as shown below. To unpin a segment, select **Unpin** (shown in red).

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-dynamic-segment.png "Dynamic segment")
   
## Exploring a segment: Viewing processing history and segment members

Select a segment's name in the **Segments** page to get to the page that is shown below. This page consolidates data at the segment level. The upper part of the page includes a trend graph that specifies changes in this segment's members count. In addition, hovering over each data point will show the member count for that point. Lastly, above the graph you can find the current member count as well as last week's growth. 

As highlighted in red below, you can adjust the trend's time scope as well (30 last days, 60 last days, etc.):

> [!div class="mx-imgBorder"] 
> ![](media/segment-time-range.png "Segment time range")

The lower part includes a table with all your segment's members.

- Note that the specific fields that appear in this table are based on the attributes of your segment’s entities. The example that is shown above (highlighted in blue) is typical for a **Customer** entity but it is only one of many possible representations.

- Also note that this table only shows a preview of your records. It presents the first 100 records of your segment so you can quickly evaluate your segment and go back to the segment editor screen to change its definitions. As we will see in the next section, exporting your segment will produce a file that includes all your records.
 
## Next Step

Go to **Segment Export** and learn how you can start acting on the insights you have just unlocked via the Segments capability. You can also explore the **Customer Card** and **Connectors** sections where you will learn to extract insights on the individual customer level

# Segment Export

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Now that you have created one ore more segments using the **segment builder** screen, you are ready to start acting upon your data  (make sure to first visit the **Segments** section if you havn't done so). 

At present, you can export any of your segments to both a CSV. file and a Customer Engagement location. In the future we will add addtional segment export options.

1. Both options are available within the **Segments** page.
      
   - First, select (...) within a specific segment's tile (shown in red below).
   - Then, select the **Export** option from the actions menu (shown in blue).
   - Lastly, choose between a CSV format and a specific Dynamics 365 for Sales destination (shown in green below). Note: Currently, only Dynamics 365 for Sales destinations are supported. 
      
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-csv.png "Segmentation export")
      
   To add a destination, use the **Export Screen** as explained below. This screen is accessible via the **Export Segment** tab on the left-side menu.
      
2. The CSV option is also available in the specific segment's page by selecting **Export** at the top-right corner of the page.

   > [!div class="mx-imgBorder"] 
   > ![](media/segment-menu-export-top.png "Export segment")
    

## Adding a segment export destination

1. Within the **Segment Export** page, select **Add Destination**.

   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-add-destination.png "Segmentation add destination")

2. Give your destination a recognizable name, define its URL, and then select a Dynamics 365 for Sales account.

   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-destination.png "Segmentation export destination")

3. Upon the completion of Step 3, your destination should appear in the **Destinations** table. Below you can see an example with three created destinations. Beyond the details completed in Step 2, this table also specifies the creation date and time for your destinations.

   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-destination2.png "Segmentation add destination")
    
   Your saved destination will also appear in the **Segments** page under the export option we explored earlier.
   
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-destination3.png "Segmentation destination")
   
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-in-process.png "Segmentation export in process")
    
   Upon clicking your Dynamics 365 for Sales destination (shown in red above), you should wait until the exporting process has completed. As long as it's in progress you can expect to see the following message.
  
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-in-process.png "Segmentation export in process")

## View segments you have exported

That can be done in the **Segment Export** page. Below the **Destinations** table you can find another table, called **Exported Segments** which specifies important information around the segments you have exported.
    
> [!div class="mx-imgBorder"] 
> ![](media/segmentation-export-segments.png "Segmentation export segments")

## Delete a destination

That can be done via **Delete** in the **Segment Export** page.


