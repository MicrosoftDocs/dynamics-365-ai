---
title: "Preview: Data Manager | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/1/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# Preview: Data Manager

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

## Data Manager Sections
**Those include: *Get Data* and *Entities*** Completing those sections will ensure that you loaded all the data that matters to you into Customer 360.  

## Data Manager: Get Data
In this section we will explain how to bring data from many of your sources: From CRM systems, to transactional and survey data, to clickstream, social and other data you might have. Connecting your data sources is the first step towards unlocking one of the unique product promises - consolidating and reconciling data on your customers from multiple sources that once were disparate and conflicting.

-	**Step One: Dataflow Creation:** Clicking the **Get Data** button will take you to the **Dataflow Screen** as shown below. You can consider dataflow to be a resource pool that is created in the system for your application usage.                                         - **If it’s the first time you are using Customer 360**, you need to create a dataflow and that is available through the highlighted **Add Entity** button:

[]

Then you should give your dataflow a name and short description as shown below:

[]

Lastly click your new dataflow to start ingsting entities into this dataflow.                                                            - **If it’s not the first time you are using Customer 360**, you should use this screen either to create a new dataflow or select an existing one. 

- **Step Two: Identifying and adding Entities**: Within the datasources page that is shown below you should locate the specific sources that apply to your organization. First identify their types which are represented by the tabs at the top of the page (highlighted below). Then, search for your specific sources under the relevant tabs and complete all the required fields for each one of them. Lastly, approve by selecting **Next** at the bottom of the page.

> [!div class="mx-imgBorder"] 
> ![](media/choose-data-source-menu.png "Data source menu")

At any point you can also remove a datasource from your dataflow by clicking the dataflow and ?

- **Step Three: Editing Entities**: You can edit any entity that you have ingested in step two. Deleting this entity, adding columns, changing columns, combining tables, and many other changes are available at your fingertips. In order to edit an entity:
    - First click the entity that you wish to edit
    - Then click **Edit Entity** as shown in red below. Note that this screen is where you can also refresh an entity's data (highlighted in blue)
[]
    - Lastly, you will use the **Power Query** editor that is shown below for the editing process. Editing columns, combining tables, and all other functionalities are available in the menu at the top of the screen as shown in red. 
[]
     
If you are new to power query, you might want to spend a couple of minutes on the following documentation that will walk you through these functionalities:
complete link

-	**Step Four: Dataflow Refresh:** Once finishing selecting data sources, you will get back to the dataflow screen. The final step is to hit the **Refresh** button as shown below:
[]

In the future this step will happen automatically.

## Data Manager: Entities
After ingesting the data, you can quickly evaluate how complete and useful it is using the **Entities** page. If you suspect that your ingested data is not complete or useful enough, you can import more data using **Add** button as highlighted below. You can also export the entities table as a .csv file by selecting **Export Data**.

> [!div class="mx-imgBorder"] 
> ![](media/scorecard-entities-import-data.png "Entities import data")

The ***Entities*** screen includes five columns (explored from left to right): 
- **Name**: The names of your data entities. Those may range from Account to Activity to many other categories. Moreover, note that if there is a warning sign next to one of the entities names, it implies that the data for that entity didn't load successfully. 
- **Last Updated**: Answers the question: *"When was the last time this entity's data was refreshed"?*
- **Source**: Answers the question *From what datasource this entity was ingested?* (csv file, Azure datasource, etc)
- **Type**: The types of your data entities. In some cases will be the same as your entities names while in others can be different.
- **Updated By**: Answers the question: *By who this entity's data was refreshed?*

The app automatically identifies values for these four columns within your ingested data sources and if the identification fails it returns *NA*. Both for *NA* and all the other values, it is recommended to go over the table and make any corrections to it as needed.

## Exploring a specific Entity's data
If you wish to explore the different fields and records that one of your entities includes click that entity. That will take you to the following screen:

Add image 9 from the 10/15 list
[]

Within this screen:
- If you click the ***Fields*** tab, you will be able to view the details of each field and field including the fields' names, data types and types.
[]

- If you click the ***Data*** tab you will be able to view the details of each record including the record's value, when it was created and when was it's last refresh.
[]
