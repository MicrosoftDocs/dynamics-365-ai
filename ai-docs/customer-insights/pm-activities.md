---
title: "Timeline | MicrosoftDocs"
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
# Timeline

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The Timeline capability consolidates customers' **activities** from multiple channels. It includes two components which we will explore in detail under this section:

1. **Timeline Screen**: This component is accessable via the timeline tab on the app left-side menu and is used to **define the activities that you wish to view around your customers**. As we will see, this definition process is done on the entity-level.
2. **Timeline Grid within the Customer 360 Dashboard**: This grid consolidates all the activities of one customer in a chronological manner. In this section we will cover the specific control you should use within the customer 360 dashboard to create the timeline grid. For guidance around the creation of the Customer 360 dashboard, please visit the **connectors** section.

## Timeline Screen
The entities that were ingested into Customer 360 might include fields with information on various activities. You should utilize this screen for the definition of the specific activities that you wish to view around your customers.

### Activity Definition
Next we will specify steps for creating a timeline activity. At any time you can save your activities through the **Save** button (highlighted in blue below), or discard the changes you have made since the last save through the **Discard** button (highlighted in red below)

> [!div class="mx-imgBorder"] 
> ![](media/activities-add-entity.png "Activities add entity")

- **Step 1: Entity selection**
Here we will choose the entity that includes our target activity or activities.
   - First, click the **Add Entity** button:
 
     > [!div class="mx-imgBorder"] 
     > ![](media/activities-search-entities.png "Activities search entities")

   - Then, **choose an entity in the entities panel.** You can also search for your entity's name via the search field (highlighted below):

     > [!div class="mx-imgBorder"] 
     > ![](media/activities-entities-define.png "Activities define entities")

   - Lastly, click the **Done** button. Upon clicking it you can notice the creation of a first row of required selections which we will complete in step two.
 


  
- **Step 2: Activity Definition**
This step includes all your activity definitions. We will explore those from left to right (see image below):

  - **Entity** (no selection is needed): Specifying your chosen entity's name
  - **Source**: (no selection is needed): Specifying your chosen entity's data source name
  - **Primary Key**: Here you should choose the specific field that includes data on your activity (in the example below, *contactId* was chosen as the activity filed in our dataset)
  - **Show Activity by**: The specific position where your activity will be placed on the timeline depends either on the starting time or ending time that you provide. Using this field, choose which of the two options will serve as the primary method for placing the activity on the time grid (in the example below, *Start Time* was chosen as the primary method)
  - **Start Time OR End Time:** Depends on your previous selection, at this point you should state the activity start/end time (only one field is required but you can select both times if those are known for your activity
  - **Duration**: Here you should define the duration of your activity 
  - **Unit**: Here you should choose the unit of time for the duration of your activity
  - **Description**: This field enables you to provide a recognizable name for your activity, so you can easily identify it on the Customer 360 Dashboard timeline 
  - **Icon**: For the same purpose of easily distinguishing your activity from the rest of your activiites, here you can add an Icon to your activity if it's publicly available (a URL address or unicode is required)
  - **X button**: Clicking this button will delete that specific activity (highlighted below)
  
    > [!div class="mx-imgBorder"] 
    > ![](media/activities-entities-close.png "Activities entities close")
  
At this point you are ready to define your next activity which can be done via the **Add** button as highlighted in red below. Don't forget to save your activities (shown in blue):

> [!div class="mx-imgBorder"] 
> ![](media/activities-add-save-entity.png "Activities entities add and save")

## Customer 360 Dashboard Timeline
Once inside the Customer 360 dashboard, you can start viewing the activities timeline for that specific customer.

// image 8

### How to Populate the Timeline component on the Dashboard
That can be done via the right side panel. 

- First, choose the **unified Activity** entity in the entities field:
    
// image 9

- Then, ..
   
### Exploring the Timeline 
The timeline diagram includes the activities that you defined on the **timeline screen** in chronological order. Each of your customer's activities includes the following detials:

// image 10

- **1.Activity Display Name**: In the example above it is
- **2.Activity Start time or End time**: In the example above it is
- **3. Activity Type**: This type was auto-identified for your activity and falls under one of six general categories. Those categories can be found above the timeline diagram:

// image 11

- **4. Activity Duration**: In the example above it is

### Filtering Timeline Activites
In addition, you can choose to include on your timeline specific set of your defined activities. The filter field on the right side panel servs that goal:

// image 12

Here you can filter by one of the following options:
- Customer ID
- Activity Type
- Activity Time?





 
