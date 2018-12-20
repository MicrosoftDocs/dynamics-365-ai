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

The Timeline capability consolidates customer activities from multiple channels. It includes two components:
- **Defining Activities** to be included in the timeline: This is done via the **Timeline screen** (accessable via the timeline tab on the app left menu). This definition process is done on the entity-level.
- **Viewing a timeline for a specific customer** (consolidation of multiple activities chronologically organized on a time grid):       This is done via the creation of a Customer 360 dashboard through the PBI connector. In this section we will cover the specific control you should use within the customer 360 dashboard. For guidance around the creation of the dashboard, please visit the connectors section

## Timeline Screen
The entities that you ingested to Customer 360 might include fields with information on various activities. You should utilize this screen for the definition of the specific activities that you wish to include in the Customer 360 dashboard timeline.

// image 1

### Activity Definition
Next we will specify the two required steps for creating each of your timeline activities. At any time you can save your activities through the Save button (highlighted in blue below), or discard the changes you have made since the last save through the Discard button (highlighted in red below)

// image 2

- **Step 1: Entity selection**
In this step you should choose the entity that includes the field you wish to include in the timeline. 
  - First, click the **Add Entity** button:
  
// image 3

  - Then, **choose an entity in the entities panel.** You can also search for your entity's name via the search field (highlighted below):

// image 4

  - Lastly, click the **Done** button. Upon clicking that button you should notice the creation of a first row for your first activity defnition (which you will complete in step 2).
  
// image 5
  
- **Step 2: Activity Definition**
This step includes all your activity defnitions. We will explore those from right to left:

  - **Entity** (no selection is needed): Specifying your chosen entity's name
  - **Source**: (no selection is needed): Specifying your chosen entity's data source name
  - **Key field**: Here you should choose the specific field that includes data on your activity (for example..)
  - **Activity Time**: The specific position where your activity will be placed on the timeline depends either on the starting time or ending time that you provide. Using this field, choose which of the two options will serve as the primary method for placing the activity on the time grid.
  - **Start Time OR End Time:** Depends on your previous selection, at this point you should state the activity start/end time (only one field is required but you can select both times if those are known for your activity
  - **Duration**: Here you should define the duration of your activity 
  - **Unit**: Here you should choose the unit of time for the duration of your activity
  - **Title**: This field enables you to provide a recognizable name for your activity, so you can easily identify it on the Customer 360 Dashboard timeline (also called display name). 
  - **Icon**: For the same purpose of easily distingushing your activity from the rest of your activites, here you can add an Icon to your activity if it's publicly available (a URL address is required)
  - **Action**: Clicking this button will delete that specific activity.
  
At this point you are ready to define your next activity. Don't forget to save your activites.

## Customer 360 Dashboard Timeline
Once inside the Customer 360 dashboard, you can start viewing the activities timeline for that specific customer.

// image 6

### How to Populate the Timeline component on the Dashboard
That can be done via the right side panel. 

- First, choose the **unified Activity** entity in the entities field:
    
// image 7

- Then, ..
   
### Exploring the Timeline 
The timeline diagram includes the activities that you defined on the **timeline screen** in chronological order. Each of your customer's activities includes the following detials:

// image 8

- **1.Activity Display Name**: In the example above it is
- **2.Activity Start time or End time**: In the example above it is
- **3. Activity Type**: This type was auto-identified for your activity and falls under one of six general categories. Those categories can be found above the timeline diagram:

// image 9

- **4. Activity Duration**: In the example above it is

### Filtering Timeline Activites
In addition, you can choose to include on your timeline specific set of your defined activities. The filter field on the right side panel servs that goal:

// image 10

Here you can filter by one of the following options:
- Customer ID
- Activity Type
- Activity Time?





 
