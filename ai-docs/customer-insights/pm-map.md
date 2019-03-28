---
title: "Map | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/26/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
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
# Map

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

There are two main goals of the map phase:

- **Entity selection:** Identify the entities that can be combined to lead to a dataset with more complete information about your customers.
- **Attribute selection:** For each entity, identify the columns (the items in those columns are called *attributes*) you want to combine and reconcile in the next data unification phases, match and merge .

<!--note from editor: In bullet item above, is it the columns that are attributes or the items listed in the columns? Nimrod will handle   -->

Select the **Map** tile on the **Unify** page to start the map phase.

## Select first entities

Start the map phase by selecting **Add entities**.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-entities.png "Add entities")

On the next screen, choose the entities you want. 

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-entities-example.png "Add entities example")

In the preceding example, the user searched for the **Contact** and **Survey** entities, since these include information that might be valuable to combine. An example might be understanding what address corresponds to what survey participant (given that the **Address** attribute exists only in the **Contact** entity). 

Then, the user selected the **Contact** and **Survey** entities. Those were found within the **Dynamics** and **Surveydata** data sources that were ingested through the **Data sources** page. 

Lastly, the user selected **Save**.

> [!NOTE] 
> You should search for and select at least two entities in order to benefit from the data unification process.

## View system auto-selections

The following page appears after you select your entities.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-ingested-entities.png "Ingested entities")

- On the left, you can see your ingested entities. By default, the first entity is auto-selected (**ContactCSV** in the preceding example). To move to any other entity, select that entity's tile. 

- Note that the system auto-selected all the attributes for which an attribute type was auto-identified. Those attributes include names, email address, and several others in the preceding example. Shown outlined in red, those preselected attributes appear in the first column, while their types are specified in the third column. You should review those preselected attributes since they will be used to combine your entities in the *match* configuration phase. 

## Add and remove attributes

Use **Edit** to add and remove attributes.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-map-edit.png "Edit map")

After you select **Edit**, the **Attributes** panel opens.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-map-contact-attributes.png "Columns for Contact")

Use **Search** or scroll down the **Attributes** list to locate and select your attributes of interest. Finish by selecting **Save**. Note that you can also choose all attributes by selecting **Select all**. Once one attribute is selected, the same button can be used to clear all your selections (now appears as **Clear all**).

<!--note from editor: Last sentence in para above is unclear to me--checkbox button turns into a Clear all button? Nimrod comment: Yes. Vivek, have an idea how to make it clearer? -->

## Add and remove entities

Use **Select** to either add or remove entities.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-edit.png "Select Edit")

Select the entities that you want to add to your existing entities list, and clear entities that you want to remove.

>[!NOTE]
>Currently, it's not possible to remove entities from the **Map** page if they were already matched on the **Match** page. 

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-edit-customer-entity.png "Select Customer entity")

## Select primary keys and define attribute types

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-configure-map-add-attributes.png "Manually add attributes")

There are two selections you must complete prior to the completion of the map phase.

- **Primary key:** (selected in the preceding example). It is mandatory that you select one attribute as a primary key for each of your chosen entities. Note that for an attribute to be a valid primary key, it should not include either duplicate values, missing values, or null values. 
- **Attribute type:** Categories of your attributes, such as email address or name. Adding a custom entity type is also possible. Select the type field for that attribute, and type your custom attribute-type name. You can also change the attribute types that were auto-identified by the system.  

### Next step
<!--note from editor: Add links to topic cross-refs   -->

As part of the data unification process, go to the **Match** page by selecting **Match** in the left-side menu or by selecting the **Match** tile on the **Unify** page. Visit the **Match** section to learn about this phase.
