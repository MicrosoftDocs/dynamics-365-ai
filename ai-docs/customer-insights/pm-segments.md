---
title: "Segmentation| MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/31/2018
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
robots: noindex,nofollow
---
# Segmentation

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Segmentation provides ability to group your customers into cohorts that match a filter criteria based on various customer attributes such as their demographic, transactional or behavioral attributes to target specific actions such as promotional campaigns or surveys to achieve desired business goals. Segments allows defining complex filter conditions based on the conflated customer entity and its data graph of related entities ingested from various data sources. Each segment after processing outputs set of master customer entity records, matching the various filter criteria defined in the segment.

There are two types of segments:

- **Static**: Segment with filter conditions that are processed once either upon the creation or update any of its filter conditions. Such segments are especially useful for cases when properties are not expected to change over time or that are expected to used ony once. Example use case: Customers who attended an expo event. 
- **Dynamic**: Segment with filter conditions that are processed according to a recurring schedule. These segments are especially useful when customers attributes change over time to continuosly update segment and keep targeting newly added customers   Example use case: customers who have bought products worth more than $500 in the last 3 months. The current dynamics segment resfreshing schedule is every 12 hours.

**How is segment defined**
Each segment is defined by combining various filter criteria that customer and its related data called data graph must match to qualify to be a member of the segment. Segment Editor provides an experience to easily define these filter criteria over the entire data graph using one or more groups. 

**What is a segment group**
Each segment group produces a set of customers based on its filter criteria. Each group's filter criteria is defined by choosing a starting entity anywhere in the customer data graph and defining filter criteria as you navigate over data graph using entity relationships to end on customer master entity - to output customer records that the group filter will produce. Multiple filter groups can be combined using set operations - union, intersect or exclude to build complex criteria using ease of set operations. 

The example below illustrates how to build a segment that uses multiple groups to define filter criteria over different part of the customer data graph. The purpose is to define a segment for customers who have placed order of more than $500 in last 90 days and had an escalated case in last 30 days so they can be followed up for satisfaction survey.

{Example of complex segment with multiple groups}
{Insert segment definition image highlighting Group 1 and Group 2}

- Group 1 uses Order as starting entity to define filter criteria to find customers who placed order for more $500 in the last 90 days
- Group 2 uses Case as starting entity to define filter criteria to find customer who have an escalated case in last 30 days

This section below will cover segment creation followed by segment exploration.

## Creating segments from the segment page
In order to start creating a segment, you can either click **Add Segment** at the top right corner of the screen (shown in red below), or click the **Get Started** button (shown in blue below).

[replace with segments 1]:
> [!div class="mx-imgBorder"] 
> ![](media/add-segment-full.png "Add segment")

If you clicked **Add Segment** then you will also need to select whether you want to create a **Static Segment** or a **Dynamic Segment** at this point.

- **Segment creation process**:
The segment creation process is executed within the **Segment Editor Page**:

> [!div class="mx-imgBorder"] 
> ![](media/new-dynamic-segment.png "New dynamic segment")

- **We start by defining the segment's properties**: We will give our segment informative name and description that will help us identifying it in the future when we will have multiple segments. Then, if we wish to change the segment's type **from Static to Dynamic or vice versa** we can do that by clicking the slider as shown in red below: 
     
> [!div class="mx-imgBorder"] 
> ![](media/new-dynamic-segment-hilites.png "Change segment type")
     
- **In step two, we will start creating our first filter**. Use the "filter" field that is shown above (highlighted in blue) to select an entity. Once we selected an entity type, we need to choose the specific attributes by which we wish to filter our customers. Note that attributes can have one of four value types: A numerical, a string, a date, or a boolean. In the example below, an attribute with a numerical value is used as a filter:
     
> [!div class="mx-imgBorder"] 
> ![](media/customer-group-numbers.png "Customer group filter")

|Number |Definition  |
|---------|---------|
|1     |Entity type         |
|2     |Attribute type         |
|3    |Operator         |
|4    |Value         |

     
- **In step three, which is optional, we will add more conditions to our filter**. We can combine our conditions in one of two ways: 
    - ***AND***: Under this option, both conditions must be met as part of the segmentation process. This option is most useful when you define two conditions for two different entities.
    - ***OR***: Under this option, either one of the conditions need to be met as part of the segmentation process. This option is most useful when you define two conditions for the same entity as examplified below:
     
> [!div class="mx-imgBorder"] 
> ![](media/customer-group-more-roles.png "Customer group with more roles")

Note that as you add conditions around more entities, **those entities are linked in a predefined manner**. As described in the Relationships section, **System Relationships** were created during the *Merge* phase and it's also possible that you created additional **Customized Relationships** through the *Relationships Screen*. As shown in the example below, based on the relationships that were created prior to segmentation, a specific path was created. 

That path dictates that you can choose to include all the records for the (Master) **Customer** entitiy as well as for the **Contact** entity, but not for the **Orders** entity since this entity carries the highest level of granularity

[segmentation 2]

- **In step four, we will show how to combine multiple filters that are created for multiple entities**. Upon selecting **Add Group**, three options will show up: ***Union***, ***Intersect*** and ***Exclude***. Clicking each of these options will result in the creation of a new filter for a new entity and the consolidation of this new filter with the filter we created in steps 2-3. 
   
> [!div class="mx-imgBorder"] 
> ![](media/customer-group-add-group.png "Customer group add group")
   
  - Choosing ***Union*** will dictate that the new segment will be fully added to the older segment - no data will be excluded:
       
  > [!div class="mx-imgBorder"] 
  > ![](media/customer-group-union.png "Customer group add union")

  - Choosing ***Intersect*** will dictate that the new segment will be combined with the older segment but if there are missing values among one of the segments, those values will be excluded.

  - Lastly, choosing ***Exclude*** will dictate that the new segment will be combined with the older segment but if there are missing values among one of the segments, those values' columns will be excluded including all their values (both missing and existing values).

## Exploring segments from the Segments page
Here you can view all your segments as well as suggested segments. These are the page components:
- **Your saved Segments:** Dynamic Segments appear to the left and Static Segments appear to the right. Each segment is represented by a tile that includes the segment name, segment description, last date of data refresh, trend (if exist), the possibility to refresh the data for that segment, and several other possibilities (highlighted in red below) that can be accessed via  <b>...</b> as highlighted in blue below:

> [!div class="mx-imgBorder"] 
> ![](media/segment-menu-hilite.png "Segment menu")

Those other options include:
    - Editing this particular segment
    - Viewing it's members
    - Exporting the segment to a .csv file
    - Turning the segment to inactive/active (depends on it's current state)
    - Deleting the segment
    
- **Recommended segments**: Those appear at the lower part of the page as shown below. Those are suggestions that are curated based on your specific customers base. Clicking *Add Segment* in each of the tiles will enable you to build segments for that specific suggestion

> [!div class="mx-imgBorder"] 
> ![](media/recommended-segments.png "Recommended segments")

## Exploring a segment: View processing history and segment members from the Segments page
Once you selected a segment within the *Segments page*, you will get to this page that consolidates everything around that particular segment. As shown below, the upper part includes a trend graph with the possibility to adjust the trend time scope (30 last days, 60 last days, etc.) with the button at the upper-right corner of the tile:

> [!div class="mx-imgBorder"] 
> ![](media/segment-time-range.png "Segment time range")

The lower part includes a table with all your segment members properties. Those include: 
- Members Names
- Members Addresses
- Members Job Titles
- Members Telephone Numbers
- Members Cities
- Members States
- Members Locations

## Acting upon the data: Exporting a segment
Exporting a segment to .csv file is possible either through the *Segments page* by selecting <b>...</b> within a specific segment's tile (shown below, upper image), or by entering the specific segment page and selecting **Export** at the top-right corner of the page (shown below, lower image):

> [!div class="mx-imgBorder"] 
> ![](media/segment-menu-export.png "Export segment")

> [!div class="mx-imgBorder"] 
> ![](media/segment-menu-export-top.png "Export segment")

Once exported, you can expect to find all the information on that particular segment within the .csv file. An example is shown below:

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-page.png "Segmentation page")
