---
title: "Map| MicrosoftDocs"
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
# Map

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]


There are two main goals behind the **Map phase:**
- **Entity selection:** Identifying the customer entities which, upon unification, may lead to a dataset with a more complete information on your customers
- **Attribute selection:** For each customer entity, identifying the columns upon which you will want to combine your data in the next phase (those columns are also called **Attributes**)

Clicking the **Map** tile at the **Configure Data page** will take you to the **Entity Selection** screen:

[Map final 1]

### Adding Entities to the Map Screen

Within the Entities Selection screen, click **Add Entites** as shown below:

[Map final 2]

Upon clicking the **Add Entities** botton, a side menu will show up on the right:

[Map final 3]

Here you want to add all the entities which, upon unification, may lead to a better understanding of your customers. 
- Within the example that is shown below, the user has searched (through the highlighted search field) for the **Contact** and **Survey** entities since these include information that might be valuable to combine. One example might be understanding what address corresponds to what survey participant (given that **Address** exists only in the **Contact** entity). 

[Map final 4]

- Then, the user has selected the **Contact** and **Survey** entities. Those were found within the **Dynamics** and **Surveydata** data sources that were ingested during the **Get Data** phase. The user has selected those two entities and clicked **Save**:

[Map final 5]

- Note that you should search for and select **at least two entities** in order to benefit from the Data Configuration process.

### Working with the Map Screen

Following entity selection, you should reach the following screen which is called the **Map Screen**:

[Map final 6]

On the left you can see your ingested entities as highlighted in red above. Upon reaching this page, the first entity will be automatically selected (in the example above it's the **Contact** entity). 

- At this point you should start add attributes to each of your entities. You should selce the attributes on the basis of which you will want to merge your entities as part of the next Data Configuration phase (called **Match**). You can either manually add attributes by selecting **Define my Own** as shown in red below, or let the system auto-identify the attributes for that entity as shown in blue.

[Map final 7]





Clicking each of the customer entities tabs on the left will open it's corresponding attributes table. Below we will explore each of this table's columns, going left to right:
- **Primary Key:** For executing the identity-resoultion process it's mandatory to **select one attribute as a unique key** for each of the customer entities. For example, if one of your data sources is a *Contacts* dataset, you may want to assign *Customer Name* as the unique key for that source, while for a *Call-Logs* file you may prefer to define *Phone Number* as a unique key. 
- **Name**: The attribute name
- **Type:** Categories under which your attributes fall such as email or name. Adding a custom entity type is also possible: Upon clicking the type for a given attribute and selecting **Custom** you will be able to type your custom type
- **Normalize:** Optional column. Here you can select whether and how to normalize all the data that you use for the matching process. Several options are available such as removing whitespaces, normalizing digits, removing punctuation, and others. 

In addition, three additional actions are available in the Map page.

![add-custom-entity.png](media/add-custom-entity.png)

- **Add customer entity:** Available upon clicking the **Add** drop-down menu (shown above). If you think there are additional entities on the basis of which your data should be merged, you should add them at this point.
    - Using the customer entities panel (shown below), first you want to click on the data source from which you wish to add more customer entities. In the example below, clicking the *Dynamics* data source opened a list with all the entities for that source. You may also use the search button to find a specific entity.
    
    - Next, you want to select the entities that you want to add. In the example below (right image) few entities have been selected.

      ![add-entity.png](media/add-entity.png)

    - Lastly, you want to save your selection and now these will be added as new tabs to the left of the entity table. 
      
      ![add-entity2.png](media/add-entity2.png)
- **Add attributes to an existing customer entity:** Available upon clicking the **Add** drop-down menu (as shown below). Choosing this option for one of your customer entities will enable you to take more attributes into consideration as part of the matching process. [UX is not ready for selection panel]

![add-attribute.png](media/add-attribute.png)

![add-attribute2.png](media/add-attribute2.png)

- **Keep unmatched records:** As part of the next stage (match), it is possible that not all of your data entities will be matched. Upon checking this box (shown below), you choose to save all the records (or dataset rows) of your unmatched entities in your master data profile for future use. This option is recommended if.. [(to complete)] 

> [!div class="mx-imgBorder"] 
> ![](media/map-keep-unmatched-records.png "Mapping - keep unmatched records")
