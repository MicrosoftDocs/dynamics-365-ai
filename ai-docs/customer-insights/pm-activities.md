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

The Activities capability consolidates customers' activities from multiple channels. It includes two components.

1. **Activities page**: This component is accessible via the **Activities** tab on the left-side menu and is used to define the activities that you wish to view around each of your customers. 
2. **Timeline grid**: This grid consolidates all the activities of one customer in a chronological manner and can be viewed either within a Customer Engagement app via the Customer Card add-in or within a Power BI dashboard. A specific control is used for the creation of that grid. Visit the **Timeline Control** section under **Extensibilities** to learn on how to work with that control. 

In this section we will only cover the **Activities** page. 

## Activities page

The entities that were ingested into Customer Insights might include fields with information on various activities. You should utilize this screen for the definition of the specific activities that you wish to view around your customers.

### Activity definition

Next, we'll specify steps for defining an activity. 

**Step One: Entity selection**

Here we will choose the entity that includes our target activity or activities.

1. First, select **Add Entity**.
  
   > [!div class="mx-imgBorder"] 
   > ![](media/activities-add-entity.png "Activities add entity")

2. Then, choose an entity in the entities panel. You can also search for your entity's name via the search field (highlighted below).
   
   > [!div class="mx-imgBorder"] 
   > ![](media/activities-search-entities.png "Activities search entities")

3. Lastly, select **Done**. Once selected, you'll see the creation of a first row of required selections which we will complete in Step Two.
 
   > [!div class="mx-imgBorder"] 
   > ![](media/activities-entities-define.png "Activities define entities")

**Step Two: Activity definition**

This step includes all your activity definitions. We will explore those from left to right.

> [!div class="mx-imgBorder"] 
> ![](media/activities-entities-close.png "Activities entities close")
    
- **Entity** (no selection is needed): Specifying your chosen entity's name.
- **Source** (no selection is needed): Specifying your chosen entity's data source name.
- **Primary key**: Here you should choose the specific field that includes data on your activity. In the example below, **contactId** was chosen as the activity filed in our dataset.
- **Show activity by**: The specific position where your activity will be placed on the timeline depends either on the starting time or ending time that you provide. Using this field, choose which of the two options will serve as the primary method for placing the activity on the time grid (in the example below, *Start Time* was chosen as the primary method).
- **Start time or end time:** Depends on your previous selection. At this point, you should state the activity start/end time. Only one field is required but you can select both times if those are known for your activity.
- **Duration**: Here you should define the duration of your activity. 
- **Unit**: Here you should choose the unit of time for the duration of your activity.
- **Description**: This field enables you to provide a recognizable name for your activity, so you can easily identify it on the Customer Insights Dashboard timeline. 
- **Icon**: For the same purpose of easily distinguishing your activity from the rest of your activities, here you can add an icon to your activity if it's publicly available. A URL address or Unicode is required.
- **Delete button**: Selecting the button that is highlighted in the image above will delete that specific activity
  
At this point you are ready to define your next activity which can be done via **Add** as highlighted in red below. Don't forget to save your activities (shown in blue).

> [!div class="mx-imgBorder"] 
> ![](media/activities-add-save-entity.png "Activities entities add and save")
   
## Next Step

Once defining your activities, you can either explore the **Timeline Control** section in order to learn how to view information on these activities for each of your customers. Viewing this information can be done on:

1. A Customer Engagement app via the Customer Card add-in. Visit the **Customer Card Add-in** section to learn how to set up the customer card.
2. The Power BI dashboard. Visit the **Connectors** section to learn how to set up the dashboard. 




 
