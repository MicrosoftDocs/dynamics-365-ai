---
title: "Get data| MicrosoftDocs"
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
# Data Manager

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

In this section we will explain how to bring data from many of your sources: From CRM systems, to transactional and survey data, to clickstream, social and other data you might have. Connecting your data sources is the first step towards unlocking one of the unique product promises - consolidating and reconciling data on your customers from multiple sources that once were disparate and conflicting. 

As shown below, the **Data Manager** includes two moduls: **Get Data** and **Entities**. You should click the **Get Data Tile** as shown below and complete the mandatory data ingestion process. Then you can either continue to the **Data Configuration** process or exploe the data that you have ingested through the **Entities** module that is accessable both via this screen and via the left side menu.

[2a]

# Get Data

-	**Step One: Dataflow Creation:** Clicking the **Get Data** button will take you to the **Dataflow Screen** as shown below. You can consider dataflow to be a resource pool that is created in the system for your application usage.
- **If it’s the first time you are using Customer 360**, you need to create a dataflow and that is available through the highlighted **Add Entity** button:

[2b]

Then you should give your dataflow a name and short description as shown below:

[3]

Lastly click your new dataflow to start ingsting entities into this dataflow.
- **If it’s not the first time you are using Customer 360**, you should use this screen either to create a new dataflow or select an existing one. 

- **Step Two: Identifying Data Sources**: Within the datasources page that is shown below you should locate the specific sources that apply to your organization. First identify their types which are represented by the tabs at the top of the page (highlighted below). Then, search for your specific sources under the relevant tabs.

> [!div class="mx-imgBorder"] 
> ![](media/choose-data-source-menu.png "Data source menu")

Lastly, upon clicking a datasource that you wish to ingest, you will need to complete all the required fields for that datasource. An example for Excel (.csv) file mandatory fields is shown below. Once all field are filled, approve by selecting **Next** at the bottom of the page. At any point you can also remove a datasource from your dataflow **by clicking the dataflow and then ?**.

[4]

- **Step Three: Editing Entities**: You can edit any entity that you have ingested in step two. In order to edit an entity:
    - First click the entity that you wish to edit
    - Then click **Edit Entity** as shown in red below. Note that this screen is where you can also refresh an entity's data (as highlighted in blue below):
    
[5]
    - Lastly, you will use the **Power Query** editor that is shown below for the editing process. Editing columns, combining tables, and several other useful functionalities are available in the top screen menu (as shown in red below):
    
[6]
     
If you are new to power query, you might want to spend a couple of minutes on the following documentation that will walk you through these functionalities:
[link1]

-	**Step Four: Dataflow Refresh:** Once finishing selecting data sources, you will get back to the dataflow screen. The final step is to hit the **Refresh** button as shown below:
[7]

Note: In the future this step will happen automatically. 

### Next Step: 
Now you are ready to unlock unique customer insights through the **Data Configure** sections (those include **Map**, **Match** and **Merge**). If you wish to review all the entities that were ingested as part of the **Get Data** process, review the **Entities** section first. 

