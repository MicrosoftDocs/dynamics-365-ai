---
title: "Segmentation| MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/22/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
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

## Introduction to segmentation

The segmentation capability of Customer Insights enables you to group your customers into cohorts based on demographic, transactional, or behavioral customer attributes. Using segmentation, you can target promotional campaigns, sales activities, and customer support actions to achieve your business goals. 

You can define complex filters around the Customer Profile entity and its graph of related entities. Each segment, after processing, outputs a set of customer entity records that you can export and take action on.

There are two types of segments:

- **Static**: A segment that is processed only once—either upon the creation or update of any of its filters. These segments are especially useful when properties are not expected to change over time or when they are expected to be used only once. Example use case: Customers who attended an expo event. 
- **Dynamic**: A segment that is processed according to a recurring schedule. These segments are especially useful when customers' attributes change over time. Example use case: Customers who have bought products worth more than $500 in the last three months. The current refresh schedule for dynamic segments is every 12 hours.

The following example illustrates the depth of the Customer Insights segmentation capability. We have defined a segment for customers who have placed orders of more than $500 in the last 90 days **and** who have been involved in a customer service call that got escalated in the last 30 days

Later, we will learn how to produce such segments. 

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-group1-2.png "Multiple groups")

- Group 1 uses **Order** as the starting entity in order to find customers who have placed an order for more than $500 in the last 90 days.
- Group 2 uses **Case** as the starting entity in order to find customers who have had an escalated case in the last 30 days.

<!--
> [!div class="mx-imgBorder"] 
> ![](media/segmentation-conceptual.png "System and custom relationships created during configuration")

The preceding example graph reflects system and custom relationships created during configuration. The data graph helps dictate the sequence by which segmentation filter criteria are defined within the **Segment Editor** page.
-->

The following two sections cover segment creation followed by segment exploration.

## Create segments from the Segment page

To create a segment, you can either select **Add Segment** at the upper-right corner of the screen, or select **Get Started**.

> [!div class="mx-imgBorder"] 
> ![](media/add-segment-full.png "Add segment")

If you select **Add Segment**, choose whether you want to create a dynamic segment or a static segment.

The rest of the segment creation process is done on the **Segment Editor** page.

> [!div class="mx-imgBorder"] 
> ![](media/new-dynamic-segment.png "New dynamic segment")

### Step One: Define the segment's properties

- We will give our segment an informative name and description that will help us identify it in the future, when we'll have multiple segments. 
- In the case of a dynamic segment, we can also choose to activate it at this point through the slider, as shown in the following example. An active (dynamic) segment automatically incorporates changes that are made to your data over time, while an inactive segment does not incorporate any changes that are made to your data. 

  > [!div class="mx-imgBorder"] 
  > ![](media/segments-allcustomers-status-active.png "Define segment")
   
### Step Two: Create a first group 

In Customer Insights, a group is a set of customers. 

**Define a group**

<!--note from editor:  Please clarify step 4 below--"until getting to the Customer Profile entity"  -->

1. Choose the entity that includes the specific attribute you want to segment by. For example, choose an Orders entity, since it includes an Order Value field by which we want to segment. In order to choose your entity of interest, select the field shown here.

    > [!div class="mx-imgBorder"] 
    > ![](media/segments-group1-define-filter.png "Choose entity")

2. Choose the attribute by which you want to segment. Our attribute can have one of four value types: numerical, string, date, or Boolean. In the following example, an attribute with a numerical value is used as a filter.

3. Choose an operator and a value for the attribute we chose in Step 2. In the following example, an operator, **Equals**, and value, **2**, were chosen.

   > [!div class="mx-imgBorder"] 
   > ![](media/customer-group-numbers.png "Customer group filter")

   |Number |Definition  |
   |---------|---------|
   |1     |Entity          |
   |2     |Attribute          |
   |3    |Operator         |
   |4    |Value         |

    Note that one of the segmentation strengths of Customer Insights is the variety of operators it supports. 

4. Add entities that are related to that entity until getting to the Customer Profile entity as will be shown in the example below. Note that for the completion of this step, you may need to first define relationships between entities using the **Relationships** page (see the “Relationships” section for more information). 

### Example - Group Creation
Let's explore a case in which we want to segment our customers by a specific clickstream activity attribute. In our example, it will be a session ID that is not equal to 1 (since this session was done on an older, outdated website version that is irrelevant for our current targeting efforts). This is the series of steps we should complete.

1. Select the **Select an entity** field.

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-group1-define-filter.png "Select entity field")

2. Choose your entity of interest (**ClickStreamData: WebsiteDatabase**) and the attribute by which you want to segment (**SessionID**).

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-group1-define-filter-settings.png "Choose entity")

3. Select an operator and a value as described earlier.

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-group1-define-filter-settings2.png "Choose Operator and Value")

4. Select the **ADD** operator.

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-group1-define-filter-settings3.png "Select ADD")

5. We need to create a path to the Customer Profile entity, but currently our entity (**ClickstreamData: WebsiteDatabase**) doesn't have a relationship with the Customer Profile entity. The only entity that has a relationship with our entity is **OnlineAccount: WebsiteDatabase** (shown in the following example), and so we will choose it.

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-group1-define-filter-settings4.png "Select OnlineAccount: WebsiteDatabase")

6. Select **All Records** as an operator. No value is needed under this operator:

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-group1-define-filter-settings5.png "Select All Records")

7. Select the **ADD** operator again. This time, our entity does have a relationship to the Customer Profile entity (which we will select), as shown here.

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-example-entities.png "Select ADD")

8. Select **All Records** as an operator, also for the Customer Profile entity.

   > [!div class="mx-imgBorder"] 
   > ![](media/segments-example-entities2.png "Select All Records")

At this point, we have completed the mandatory path definition. We recommend that you save your first group's definitions, as shown here.

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-save-group-definition.png "Save group definition")


### Step Three (optional): Add more conditions to your group 

The following two logical operators can be used for that purpose:

- **AND**: Under this option, both conditions must be met as part of the segmentation process. This option is most useful when you define conditions across different entities (one condition per entity) as shown here.
    
  > [!div class="mx-imgBorder"] 
  > ![](media/segmentation-both-conditions.png "Both conditions met")
    
- **OR**: Under this option, either one of the conditions needs to be met as part of the segmentation process. This option is most useful when you define multiple conditions for the same entity, as shown here.
    
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-either-condition.png "Either conditions met")

Note that currently, it's possible to nest an **OR** operator under an **AND** operator but not vice versa.

### Step Four (optional): Combine multiple groups via set operators

Each group produces a specific set of customers. Start by selecting **Add Group**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-group-add-group.png "Customer group add group")

Three set operators are displayed: **Union**, **Intersect**, and **Exclude**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-group-union.png "Customer group add union")
 
Selecting a set operator enables you to define a new group. Saving different groups determines what data gets maintained:

- **Union** unites the new group you have created in Step Four with the group you have created in Steps Two and Three. With this option, data that is common to both groups is maintained, as well as data that is not common to both groups.

- **Intersect** intersects the two groups. Only data that is common to both groups is maintained in the unified group.

- **Exclude** excludes the two groups. Only data that is not common to both groups is maintained.
   
## Explore segments from the Segments page

> [!div class="mx-imgBorder"] 
> ![](media/segments-list2.png "Explore segments")

On the Segments page, you can view all your saved segments and perform certain actions.

- Dynamic segments appear to the left, and static segments appear to the right.
- Each segment is represented by a tile that includes the segment's name, description, last date of data refresh, and historical trend (if it exists). Hover over the trendline to see last week's growth in this segment's members count. If you prefer to view all of your segments in a table format, select one of the following:
  > [!div class="mx-imgBorder"] 
  > ![](media/segmentation-static-segment.png "Static segment")

You can also perform certain actions with each segment. First, select the following button on the segment's tile:

> [!div class="mx-imgBorder"] 
> ![](media/segments-list.png "Click button in segment tile")

Then, choose one of the following options from the drop-down menu:
- Editing the segment
- Viewing the segment's members
- Exporting the segment to either a CSV file or to a Dynamics 365 for Sales location. For more information on the different exporting options make sure to visit the **Segment Export** section.
- Turning the segment to inactive or active (depending on its baseline state)
- Deleting the segment 
- Pinning the segment, which moves it to the top of the screen for better accessibility. The pinned segment appears under **Pinned Segments** as shown in the following example. To unpin a segment, select **Unpin** (shown in red).

  > [!div class="mx-imgBorder"] 
  > ![](media/segmentation-dynamic-segment.png "Dynamic segment")
   
## Explore a segment: View processing history and segment members

Select a segment's name in the **Segments** page to get to the page shown in the following example. This page consolidates data at the segment level. The upper part of the page includes a trend graph that specifies changes in this segment's member count. In addition, hovering over each data point shows the member count for that point. Above the graph, you can find the current member count and last week's growth. 

As highlighted in this example, you can adjust the trend's time scope as well (last 30 days, last 60 days, and so on).

> [!div class="mx-imgBorder"] 
> ![](media/segment-time-range.png "Segment time range")

The lower part includes a table with all your segment's members.

- Note that the specific fields that appear in this table are based on the attributes of your segment’s entities. The preceding example is typical for a **Customer** entity, but it is only one of many possible representations.

- Also note that this table shows only a preview of your records. It presents the first 100 records of your segment so that you can quickly evaluate your segment and go back to the segment editor page to change its definitions. As we will see in the next section, exporting your segment produces a file that includes all your records.
    
## Next step
Visit the **Segment Export** section to learn about the different options for exporting your segments. 
You can also explore the **Customer Card** and **Connectors** sections to get insights on the customer-level.
    

