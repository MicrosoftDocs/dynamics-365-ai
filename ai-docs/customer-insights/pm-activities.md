---
title: "Activities | MicrosoftDocs"
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
# Activities

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The **Activities** capability helps consolidate customers’ activities from various data sources, to create a customer journey which can be visualized in a timeline view. Business analysts can configure the activities that would be displayed on a custom dashboard with timeline view, which can be embedded within business applications.

It includes two components:
- **Activities page**: This component is accessible via the **Activities** tab on the left-side menu and is used to define the activities that you wish to view on the customer’s timeline grid.
- **Timeline grid:** This grid consolidates all the activities of one customer in a chronological order, and can be viewed either within a Customer Engagement app via the Customer Card add-in, or within a Power BI dashboard. A specific control is used for the creation of that grid. Visit the **Timeline Control** sub-section within the **Customer Card Add-In** section to learn how to work with that control.

In this section we will only cover the **Activities** page.

## Activities page

Your data sources include entities with transactional/activity data from multiple data sources. In this page you will identify these entities and select the activities you wish to view on the customer’s timeline grid.

### Activity definition

**Step One: Entity selection**

Here we will choose the entity that includes our target activity or activities.

1. Select **Add Entity**.
  
   > [!div class="mx-imgBorder"] 
   > ![](media/activities-add-entity.png "Activities add entity")

2. Select all the entities that include transactional/activity data. You can search by the entity's name via the search field (highlighted below).
   
   > [!div class="mx-imgBorder"] 
   > ![](media/activities-search-entities.png "Activities search entities")

3. Select **Done**. Once selected, you'll see the creation of a row per selected entity, with the required fields which we will complete in Step Two. 

   Note: to be included in the timeline grid, an entity must have at least one attribute of type Date. Entities without Date fields will not be added.
 
   > [!div class="mx-imgBorder"] 
   > ![](media/activities-entities-define.png "Activities define entities")

**Step Two: Activity definition**

This step includes all your activity definitions. We will explore those from left to right.

> [!div class="mx-imgBorder"] 
> ![](media/activities-entities-close.png "Activities entities close")
    
- **Entity** (no selection is needed): Specifying your chosen entity's name.
- **Source** (no selection is needed): Specifying your chosen entity's data source name.
- **Primary key**: This field will be used to distinguish between all of your entity's records. This field should not contain any duplicate values, *Nulls* and missing values. Few options are *ActivityID*, *SessionID* and *OrderID* but there are many other possible Primary keys.
- **Activity Name**: Select the specific field that includes data on your activity. 
- **Show activity by**: Timeline grid is sorted by date in descending order (from newest to oldest). You need to decide if you want to show the activity by Start or End time, for us to place it correctly on the timeline. Using this field, choose which of the two options will serve as the primary method for placing the activity on the time grid (in the example below, Start Time was chosen as the primary method).
- **Start time or end time:** Depends on your previous selection. At this point, you should select the field that represents the start/end time. Only one field is required but you can select both times if those are known for your activity.
- **Duration**: Select the field that represents the duration of your activity.
- **Unit**: Select the unit of time for the duration of your activity.
- **Description**: Select the field that represents a description of the activity
- **Icon**: You may add an icon to easily distinguish this activity on the timeline. You can add an icon to your activity if it's publicly available. A URL address or Unicode is required.
- **Delete button**: Selecting the button that is highlighted in the image above will delete that specific activity.
  
You may now define your next activity, which can be done via Add as highlighted in red below. Don't forget to save your activities (shown in blue).

// 1 <!-- replace red with 1 and blue with 2-->

> [!div class="mx-imgBorder"] 
> ![](media/activities-add-save-entity.png "Save and add activities entities")
   
## Next Step
Once defining your activities, you can:
1. Explore the **Timeline Control sub-section** under the **Customer Card Add-in section** in order to learn how to view information on these activities for each of your customers.
2. Visit the **Connectors section** to learn how to set up the **Power BI dashboard** where you can also view information on these activities for each of your customers.

