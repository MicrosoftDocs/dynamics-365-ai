---
title: "Measures | MicrosoftDocs"
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
# Measures

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The **Measures** page enables you to define all the KPIs that best reflect your specific business domain and goals. Once defined, you can benefit from your measures in a verity of ways. For example:
- Consume on your Homepage 
- View for a specific customer as part of the **Customer Card**. See the **Customer Card Add-in** section to learn more. 
- Use to define a customer segment, using the **Segment Builder** page. See the **Segments** section to learn more.

## Step One: Choose between three measure types

There are two early decisions you should make with regard to your desired measure. These decisions will help you choose between the three options that are available to you upon selecting **New Measure**.

> [!div class="mx-imgBorder"] 
> ![](media/search-measures.png "Search measures")

First, you should decide whether to:
  - Save your measure as an attribute within one of your existing entities. Then you should choose the **Profile Attribute** option. 
  - Or, create a new entity around your measure.
  
Second, if decided to save the measure as a new entity, you should also decide whether to:
  - Create the measure on the basis of fields from the Customer Profile entity - which corresponds to a **Profile Measure** option.
  - Or, create it on the basis of another ingested entity which corresponds to a business measure.
  
Note that your choice at this point will affect the number of dimensions supported for your measure. You will choose your dimensions in Step Four when we will go through the *Measure Definition* process. 
- Profile attribute and profile measure are limited to a single dimension.
- Business measure supports multiple dimensions.

In the next three sections, we will explore the steps you should complete in order to define your measure. 

## Step Two: Choose the base entity

After choosing an option, you'll go to the **Measure Creation** panel. For example, after selecting the **Business Measure** option, you'll see the following.

> [!div class="mx-imgBorder"] 
> ![](media/new-business-measure.png "New business measure")

- **Name** (mandatory): Upon completing the configuration of your measure, it will show up in the **Measures** page as a saved measure that you can edit. Within the **Measures** page, your saved measure will carry the name you define under the **Name** field in this panel.
- **Display Name** (optional): As mentioned earlier, your measure will also be added as an attribute or be saved as a new entity. In both cases, the measure will carry the name you define under the **Display Name** field in this panel.
- **Starting Entity** (mandatory): Here you should choose the entity on the basis of how you wish to construct your measure. If you wish to include in your measure fields from multiple entities, choose any of these entities.  

For example, here's the panel you'll see upon selecting the **Profile Measure** option.

> [!div class="mx-imgBorder"] 
> ![](media/new-profile-measure.png "New profile measure")

This panel is the same panel we explored under the previous options except for one difference: The Customer Profile entity will automatically be selected as your starting entity. This default selection can't be changed.

For example, here's the panel you'll see upon selecting the **Profile Measure** option.

> [!div class="mx-imgBorder"] 
> ![](media/new-profile-attribute.png "New profile attribute")

## Step Three: Choose related entities

Once completing Step Two, you'll see the following page.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition.png "Measure definition")

First, you should decide whether additional entities are needed as part of your measure definition. One use case might be creating an expression that will be based on attributes from two or more different entities. We will explore that use case in Step Four. Another use case, specifically for profile measure and business measure, is creating an entity for your measure that is composed of multiple entities. We will explore that use case in Step Five.

In order to choose additional entities, select **Add new entity** and pick the entities of your interest.

> [!div class="mx-imgBorder"] 
> ![](media/select-an-entity.png "Select an entity")

**Note**: You can only select entities which have relationships to your base entity. If you haven't defined relationships yet, see the **Relationships** section.

## Step Four: Calculate a variable

> [!div class="mx-imgBorder"] 
> ![](media/accounts-dynamics-365.png "Accounts Dynamics365")

Select **Add new variable** to open the **Variable Definition** panel.

> [!div class="mx-imgBorder"] 
> ![](media/new-variable-name.png "New variable name")

Let's explore the steps you should complete in this panel:

1. Give your variable a recognizable name. 
2. Select the **Expression** area.
3. Choose a field from the fields shown to the right.
4. Type an expression in the **Expression** area while choosing more fields. **Note**: At this point, we only support arithmetic expressions.
5. Select **Done**.

In the example below, we have defined a calculation for the relative contribution of a single Purchase to the Customer Lifetime Value (CLTV).

> [!div class="mx-imgBorder"] 
> ![](media/new-variable-name2.png "New variable name")


## Step Five: Define your measure entity/attribute

In this step, we will decide how to aggregate our chosen entities and calculations into a measure entity/attribute which we can start using in **Homepage**, **Segments**, as well as other pages. 

**Step 1:** Define first dimension

These are the selections you should fill in (exploring left to right the definitions shown below).

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition2.png "Measure definition")

**Entity/variable**: You should include at least one attribute in your Measures entity. Note: If you are defining a Measures attribute it can be only one attribute. This selection is about choosing either the entity that includes that attribute, or one of the variables you created in Step Four.
**Field**: Here you should pick the specific attribute/variable to be included either in the Measures entity or in another entity as a field.
**Bucket**:
**As**: Here you should define the name of your new field in the Measures entity/attribute.
**Display Name**: Here you should define the display name of your field in the Measures entity/attribute.

**Step 2 (optional)**: Add more dimensions by selecting **Add new dimension** 

> [!div class="mx-imgBorder"] 
> ![](media/new-dimension.png "New dimension")

**Step 3 (optional)**: Add measures

This option should be used in case you wish to aggregate any of your dimensions via summation, counting, etc. These aggregations will happen at the end of the selected field in your Measures entity/attribute. 

First, select **New Measure**.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition3.png "Measure definition")

Then, make those selections (exploring left to right the definitions shown below).

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition4.png "Measure definition")

**Function**: At present, we support **Sum, Min, Max, Count and Unique Count** as aggregation options.
**Entity/Variable**: You should include at least one attribute in your Measures entity. Note: If you are defining a Measures attribute it can be only one attribute. This selection is about choosing either the entity that includes that attribute, or one of the variables you created in Step Four.
**Field**: Pick the specific attribute/variable to be included either in the Measures entity or in another entity as a field.
**As**: Define the name of your new field in the Measures entity/attribute.
**Display Name**: Define the display name of your field in the Measures entity/attribute.

Save your measure.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition-save.png "Measure definition")

## View and Edit your measures 

Once completed your first measure, you'll see the following page that summarizes your created measures.

> [!div class="mx-imgBorder"] 
> ![](media/new-measure.png "New measure")

At anytime, you can create a new measure via **Add Measure** shown above.

You can also edit, delete, rename, and refresh the data of any of your created measures by first selecting the following button.

> [!div class="mx-imgBorder"] 
> ![](media/measure-menu.png "Measure menu")

Choose from the **Options** drop down menu.

> [!div class="mx-imgBorder"] 
> ![](media/measure-menu2.png "Measure menu")

Here is an example of the **Rename measures** window.

> [!div class="mx-imgBorder"] 
> ![](media/rename-measure.png "Rename measure")

The edit option is done on the same page we used to create our first measure. 

