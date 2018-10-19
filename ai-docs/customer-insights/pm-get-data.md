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
# Get data

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

In this section we will explain how to bring data from many of your sources: From CRM systems, to transactional and survey data, to clickstream, social and other data you might have. Connecting your data sources is the first step towards unlocking one of the unique product promises - consolidating and reconciling data on your customers from multiple sources that once were disparate and conflicting.

-	**Step One: Dataflow Creation:** Clicking the **Get Data** button will take you to the **Dataflow Screen** as shown below. You can consider dataflow to be a resource pool that is created in the system for your application usage.
- **If it’s the first time you are using Customer 360**, you need to create a dataflow and that is available through the highlighted **Add Entity** button:

[]

Then you should give your dataflow a name and short description as shown below:

[]

Lastly click your new dataflow to start ingsting entities into this dataflow.
- **If it’s not the first time you are using Customer 360**, you should use this screen either to create a new dataflow or select an existing one. 

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

