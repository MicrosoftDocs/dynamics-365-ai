---
title: "Segmentation| MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
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

Segmentation provides the ability to group your customers into cohorts that match a filter criteria based on various customer attributes such as their demographic, transactional or behavioral attributes. Using segmentation you can achieve more targeted actions such as promotional campaigns or surveys to achieve desired business goals. Segmentation allows defining complex filter conditions based on the conflated customer entity and its data graph of related entities ingested from various data sources. Each segment after processing outputs set of master customer entity records, which matches the various filter criteria defined in the segment.

There are two types of segments:

- **Static**: Segment with filter conditions that are processed once either upon the creation or update any of its filter conditions. Such segments are especially useful for cases when properties are not expected to change over time or that are expected to used ony once. Example use case: Customers who attended an expo event. 
- **Dynamic**: Segment with filter conditions that are processed according to a recurring schedule. These segments are especially useful when customers attributes change over time to continuosly update segment and keep targeting newly added customers   Example use case: customers who have bought products worth more than $500 in the last 3 months. The current dynamics segment resfreshing schedule is every 12 hours.

**How is a segment defined**
Each segment is defined by combining various filter criteria that customer and its related data called data graph must match to qualify to be a member of the segment. Segment Editor provides an experience to easily define these filter criteria over the entire data graph using one or more groups. 

**What is a segment group**
Each segment group produces a set of customers based on its filter criteria. Each group's filter criteria is defined by choosing a starting entity anywhere in the customer data graph and defining filter criteria as you navigate over data graph using entity relationships to end on customer master entity - to output customer records that the group filter will produce. Multiple filter groups can be combined using set operations - union, intersect or exclude to build complex criteria using ease of set operations. 

The example below illustrates how to build a segment that uses multiple groups to define filter criteria over different parts of the customer data graph. The purpose is to define a segment for customers who have placed order of more than $500 in last 90 days and had an escalated case in last 30 days so they can be followed up for satisfaction survey.

<!-- 
{final1:Example of complex segment with multiple groups}

{final2:Insert segment definition diagram created by Nimrod, highlighting Group 1 and Group 2}
-->

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-group1-2.png "Mulitple groups")

- Group 1 uses Order as starting entity to define filter criteria to find customers who placed order for more $500 in the last 90 days
- Group 2 uses Case as starting entity to define filter criteria to find customer who have an escalated case in last 30 days

> [!div class="mx-imgBorder"] 
> ![](media/segmentation-conceptual.png "System and custom relationships created during configuration")

The example data graph above reflects system and custom relationships created during configuration. The data graph helps dictate the sequence by which segmentation filter criteria are defined within the Segment Editor page.

The two sub-sections below will cover segment creation followed by segment exploration.

## Creating segments from the segment page
In order to start creating a segment, you can either click **Add Segment** at the top right corner of the screen (shown in red below), or click the **Get Started** button (shown in blue below).

<!-- [replace with segments 1]: -->

> [!div class="mx-imgBorder"] 
> ![](media/add-segment-full.png "Add segment")

If you clicked **Add Segment** then you will also need to select whether you want to create a **Static Segment** or a **Dynamic Segment** at this point.

- **Segment creation process**:
  The segment creation process is executed within the **Segment Editor Page**:

  > [!div class="mx-imgBorder"] 
  > ![](media/new-dynamic-segment.png "New dynamic segment")

- **We start by defining the segment's properties**: 
   - We will give our segment informative name and description that will help us identifying it in the future when we will have multiple segments. 
   - Then, if we wish to change the segment's type **from Static to Dynamic or vice versa** we can do that by clicking the slider as shown in red below: 
     
<!-- [Replace with final 3:] -->

  > [!div class="mx-imgBorder"] 
  > ![](media/new-dynamic-segment-hilites.png "Change segment type")

- Lastly, if we are defining a dynamic segment, we can choose to **activate it** at this point through the second slider as shown in blue above. **An active (dynamic) segment will automatically incorporate changes** that are made to your source data with time while **inactive segment will not incorporate changes to your data.** You sould activate your segment only when you wish to start incorporating changes to your data.
   
- **In step two, we will start creating our first filter**. Use the "filter" field that is shown above (highlighted in blue) to select an entity. Once we selected an entity type, we need to choose the specific attributes by which we wish to filter our customers. Note that attributes can have one of four value types: A numerical, a string, a date, or a boolean. In the example below, an attribute with a numerical value is used as a filter:
     
> [!div class="mx-imgBorder"] 
> ![](media/customer-group-numbers.png "Customer group filter")

|Number |Definition  |
|---------|---------|
|1     |Entity          |
|2     |Attribute          |
|3    |Operator         |
|4    |Value         |

Note that **one of the segmentation strengths of Customer 360 is the rich varity of operators it supports.** Here is a table that summarizes all the operators that are currently supported for the four different value types. It also specifies which operators can be combined to produce complex segmentations. Lastly, it encapsulates some examples:

<!-- [operators table - Shashi still needs to provide me an updated one] -->

- **In step three, which is optional, we will add more conditions to our group.** The following two logical operators can be used for that purpose:

   - ***AND:*** Under this option, both conditions must be met as part of the segmentation process. This option is most useful when you define conditions across different entities (one condition per entity) as exemplified below: 
    
   <!-- [final 5] -->
    
   - ***OR:*** Under this option, either one of the conditions need to be met as part of the segmentation process. This option is most useful when you define multiple conditions for the same entity as exemplified below: 
    
   <!-- [final 6] -->

Note: It is recommended to save your first group's definitions as shown below:

<!-- [final 7] -->

- **In step four which is also optional, we will show how to combine multiple groups via Set Operators**
As mentioned earlier, each group **produces a specific set of customers**. Start by selecting **Add Group**:

> [!div class="mx-imgBorder"] 
> ![](media/customer-group-add-group.png "Customer group add group")

Then three set operators will show up: ***Union, Intersect and Exclude***. Clicking each of these will enable you to define a new group. However, upon clicking **Save**, each of these Set Operators will lead to a different result:

- **Intersect** will intersect the new group with the group you have created in steps 2-3. **Only data that is common** to both groups will be maintained.

<!-- [final 9] -->

- **Unite** will unite the two groups - **data that is common** to both groups will be maintained as well as data **that is not common** to both groups**

> [!div class="mx-imgBorder"] 
  > ![](media/customer-group-union.png "Customer group add union")

- Lastly, **Exclude** will exclude the two groups - **only data that is not common** to both groups will be maintained.

<!-- [final 10] -->

- Here is an example for how **Intersect** operator can help you define a sophisticated segmentation logic that involves multiple groups:

<!-- [final 11] Optinal - under consideration -->
   
## Exploring segments from the Segments page
Here you can view all your saved segments and perform certain actions.
-**Dynamic Segments appear to the left and Static Segments appear to the right.**
-**Each segment is represented by a tile** that includes the segment's name, segment's description, last date of data refresh for that segment, historical trend (if exist) and the possibility to refresh the data for that segment.
-**You can also perform certain actions with each segment (highlighted in red below)**. These actions can be accessed via the **three dots** button as highlighted in blue below:

<!-- [final 12] -->

Let's explore those segment-level actions:
    - Editing this particular segment
    - Viewing it's members
    - Exporting the segment to a .csv file
    - Turning the segment to inactive/active (depends on it's current state)
    - Deleting the segment
    
## Exploring a segment: View processing history and segment members from the Segments page
Once you selected a segment within the *Segments page*, you will get to this page that consolidates everything around that particular segment. As shown below, the upper part includes a trend graph with the possibility to adjust the trend time scope (30 last days, 60 last days, etc.) with the button at the upper-right corner of the tile:

> [!div class="mx-imgBorder"] 
> ![](media/segment-time-range.png "Segment time range")

The lower part includes a table with all your segment members.

- **Note** that the field types that are shown in this table are based on the attributes of your segment’s entities. The example table that is shown above (highlighted in blue) is typical to a **Customer** entity but it is only one of many possible table types.

-**Also note** that this table only shows a preview of your records: It presents the first 100 records of your segment so you can quickly evaluate your segment and consider to go back to the segment editor screen and change it's definitions. As we will see in the next section, **exporting** your segment will produce a file that includes **all** your records.

## Acting upon the data

**Exporting a segment:
Exporting a segment to .csv file is possible either through the *Segments page* by selecting the **three dots** icon within a specific segment's tile and then the **Export** button as described earlier, or by entering a specific segment's page (by clicking the segment tile in the segments screen) and selecting **Export** at the top-right corner of the page as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/segment-menu-export-top.png "Export segment")

Once exported, you can expect to find all the information on that particular segment within the .csv file. An example is shown below:

<!-- [final 13] - optional -->

## Next Step
While segmentation provides you with aggragate-level insights, you can also explore the Customer 360 Dashboard to unlock varity of customer-level insights. If you wish to produce those, visit the **Connectors** section.
