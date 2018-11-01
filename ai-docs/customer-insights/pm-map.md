---
title: "Map | MicrosoftDocs"
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

There are two main goals behind the map phase:

- **Entity selection:** Identify the customer entities which, upon unification, may lead to a dataset with more complete information on your customers
- **Attribute selection:** For each customer entity, identify the columns upon which you will want to combine your data in the next phase (those columns are also called **Attributes**)

Select the **Map** tile on the **Configure Data** page to open the **Entity Selection** page.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map.png "Map tile")

### Add entities to the Map page

In **Entities Selection**, select **Add Entities**.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-entities.png "Add entities")

Select **Add Entities**.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-search-entities.png "Search entities")

Add all the entities which, upon unification, might lead to a better understanding of your customers. 

In the example below, the user searched for the Contact and Survey entities since these include information that might be valuable to combine. One example might be understanding what address corresponds to what survey participant (given that Address exists only in the Contact entity). 

Then, the user selected the Contact and Survey entities. Those were found within the **Dynamics** and **Surveydata** data sources that were ingested during the **Get Data** phase. The user selected those two entities, and then selected **Save**.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-entities-example.png "Add entities example")

> [!NOTE]
> You should search for and select at least two entities in order to benefit from the data configuration process.

### Add attributes to entities in the Map page

Following entity selection, the **Map** page appears.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-ingested-entities.png "Ingested entities")

On the left, you can see your ingested entities. The first entity is automatically selected. In the example, above it's the Contact entity. 

At this point, you should start adding attributes to each of your entities. You should select all the attributes on the basis of which you want to combine with your entities. You can either manually add attributes (**Define my own**), or let the system auto-identify the attributes for the selected entity (**Use system recommendations**).

#### Manually adding attributes**

When you select **Define**, a window appears on the right in which you can manually add attributes.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-attributes.png "Manually add attributes")

Here you can select all the attributes that are relevant for each of your entities. Remember, in the example above we had two entities: Contact and Survey. Use either **Search attributes** (red) and/or scroll down the **Attributes** menu (blue) to locate and select all the attributes. Finish by selecting **Save**. Note that you can also choose all the attributes by selecting **Select all attributes** (green). Selecting **Select all attributes** again to deselect all your chosen attributes.

[Map final 9]

## Selecting Primary Keys and Defining Attribute Types

[Map final 10]

Clicking each of the customer entities tabs on the left will open it's corresponding attributes table as shown above for the **Survey** entity as an example. Below we will explore this table's columns from left to right. Note that **It is required to make selections within all the *Mandatory* columns:
- **Primary Key (Mandatory Selection):** For executing the identity-resoultion process it's mandatory to **select one attribute as a unique key** for each of the customer's entities. For example, if one of your data sources is a *Contacts* dataset, you may want to assign *Customer Name* as the unique key for that source, while for a *Call-Logs* file you may prefer to define *Phone Number* as a unique key. 
- **Column Name**: The attribute's name as appears in the dataset
- **Customer attribute (Mandatory Selection)**: 
- **Entity Type(Mandatory?):** Categories under which your attributes fall such as email or name. Adding a custom entity type is also possible: Upon clicking the type for a given attribute and selecting **Custom** you will be able to type your custom type
- **Normalize:** Optional column. Here you can select whether and how to normalize all the data that you use for the matching process. Several options are available such as removing whitespaces, normalizing digits, removing punctuation, and others. 

## Adding or Editing Entities and Attributes

Both actions are available through the **Edit**  as shown below:

![add-custom-entity.png](media/add-custom-entity.png)

- **Add Entities:** After clicking **Edit**, select **Customer Entity**:
   
   [Map final 12]
   
Next, you want to select the entities that you want to add to your existing entities and deselect entities that you want to remove. In the example below...

[ Map final 13 - need to get final image]

- **Edit Existing Entities**:

- **Add an Attribute to an Entity**: First select the entity to which you want to add data. Then click **Edit** and select **Attributes to [Your Entity's Name]**. In the example below we are adding attributes to the **Contact** entity:

[ Map final 14]

Next you want to select additional attributes or deselect attributes you have selected in the past. In the example below we will deselect **Gender** and add **Residence Country**:

[Map final 15]

## Keep unmatched records
As part of the next stage (match), it is possible that not all of your data entities will be successfully matched. Upon checking this box (shown below), you choose to save all the records of your unmatched entities in your master data profile for future use. This option is recommended if.. [(to complete)] 

> [!div class="mx-imgBorder"] 
> ![](media/map-keep-unmatched-records.png "Mapping - keep unmatched records")

## Next Step
As part of the **Data Configuration** process, please continue to **Match** either by clicking the **Match tab** at the app left menu or by choosing the **Match tile** from the **Configure Data** screen.
