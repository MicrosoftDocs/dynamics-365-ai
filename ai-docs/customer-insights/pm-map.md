---
title: "Map | MicrosoftDocs"
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

At this point, you should start adding attributes to each of your entities. You should select all the attributes on the basis of which you want to combine your entities in the next configuration phase (*Match*). Note, for some entities the system will auto-identify recommended attributes (for example for several Dynamics 365 apps) and you can always remove those recommendations.

#### Manually adding attributes

When you click the **Edit** button, a window appears on the right in which you can manually add attributes.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-attributes.png "Manually add attributes")

Here you can select all the attributes that are relevant for each of your entities. Remember, in the example above we had two entities: *Contact* and *Survey*. Use either **Search attributes** (red) and/or scroll down the **Attributes** menu (blue) to locate and select all the attributes. Finish by selecting **Save**. Note that you can also choose all the attributes by selecting **Select all attributes** (green). Selecting **Select all attributes** again can be used to unselect all your chosen attributes.

## Select primary keys and define attribute types

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-primary-keys.png "Select primary keys")

Select each of the customer entities tabs on the left to open its corresponding attributes table as shown above for the *Survey* entity example. Below we will explore this table's columns from left to right. Note: you must make selections within all the mandatory columns:

- **Primary key (mandatory selection):** For executing the identity-resolution process, it's mandatory to select one attribute as a ***primary key*** for each of the entities. Note that in order for an attribute to be a valid primary key, it should not include either duplicate values, missing values or *Nulls*. 
- **Type (mandatory selection):** Categories under which your attributes fall such as email or name. Adding a custom entity type is also possible. Select the type for a given attribute and select **Custom**  to specify your custom type. Lastly, note that for Dynamics 365 entities, some attribute-types will be auto-identified by the system and you can always change those default definitions. 

## Edit entities list 

Click **Select** to add or edit the entities that you selected upon entering the Map screen for the first time.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-edit.png "Select Edit")

Select the entities that you want to add to your existing entities list and deselect entities that you want to remove. 

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-edit-customer-entity.png "Select Customer entity")

To add an attribute to an existing entity, first select the entity to which you want to add data. Select **Edit**, and then select **Attributes to [entity's name]**. In the example below, we are adding attributes to the Contact entity.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-edit-attributes-survey.png "Select Attributes to entity name")

## Edit Attributes List

You might want to select additional attributes or deselect attributes you have selected in the past. That can be done via the **Edit** button as before. In the example below, we deselect **Gender** and add **Residence Country**.

<!-- [Map final 15] -->

## Next Step
As part of the data configuration process, proceed to the **Match** page either by selecting **Match** in the left menu or by selecting the **Match** tile from the **Configure Data** page.
