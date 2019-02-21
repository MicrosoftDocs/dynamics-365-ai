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

The **Measures** page enables you to define all the KPIs that best reflect your specific business domain and goals. Once defined, you can benefit from your measures in a variety of ways. For example:

- Consume on your **Home** page 
- View for a specific customer as part of the **Customer Card**. See the **Customer Card Add-in** section to learn more. 
- Use to define a customer segment, using the **Segment Builder** page. See the **Segments** section to learn more.

## Step One: Choose between three measure types

There are two early decisions you should make with regard to your desired measure. These decisions will help you choose between the three options that are available to you upon selecting **New Measure**.

> [!div class="mx-imgBorder"] 
> ![](media/search-measures.png "Search measures")

First, you should decide whether to:

  - Create a new entity around your measure.
  - Or, save your measure as an attribute within the Customer Profile entity. Then choose the **Profile Attribute** option. After creating each Profile Attribute, it will be added to a new entity on the **Entities** page that includes all of your Customer Profile data plus the new attribute called **Customer_Measure**.
  
> [!div class="mx-imgBorder"] 
> ![](media/measures-customer-entity.png "Customer_Measure attribute")
.
Second, if decided to save the measure as a new entity, you should also decide whether to:

  - Create the measure based on fields from the Customer Profile entity - which corresponds to a **Profile Measure** option.
  - Or, create it based on another ingested entity which corresponds to a **Business Measure.**
  
Note that your choice at this point will affect the number of dimensions supported for your measure. You will choose your dimensions in Step Four when we will go through the *Measure Definition* process. 

- Profile attribute and profile measure are limited to a single dimension.
- Business measure supports multiple dimensions.

In the next three sections, we will explore the steps you should complete in order to define your measure. 

## Step Two: Choose the Starting entity

Upon clicking **New Measure** you will get to the **Measure Creation** panel. For example, after selecting the **Business Measure** option, you will see the following.

> [!div class="mx-imgBorder"] 
> ![](media/new-business-measure.png "New business measure")

- **Name** (mandatory): After completing the configuration of your measure, it will show up in the **Measures** page under this name.
- **Display name** (optional): As mentioned earlier, your measure will also be added as an attribute or be saved as a new entity. In both cases, the measure will carry the name you define under that field. 
- **Starting entity** (mandatory): Here you should choose the entity on the basis of which you wish to construct your measure. If you wish to include in your measure fields from multiple entities, choose any of these entities.  

Here is the panel you will see upon selecting the **Profile Measure** option.

> [!div class="mx-imgBorder"] 
> ![](media/new-profile-measure.png "New profile measure")

This panel is the same panel we explored under the previous option except for one difference: The Customer Profile entity will automatically be selected as your starting entity. This default selection can't be changed.

Finally, here is the panel you will see upon selecting the **Profile Attribute** option.

> [!div class="mx-imgBorder"] 
> ![](media/new-profile-attribute.png "New profile attribute")

## Step Three: Choose related entities

After completing Step Two, you'll see the following page.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition.png "Measure definition")

At this point you should decide whether additional entities are needed as part of your measure definition. One use case might be creating an expression that will be based on attributes from two or more different entities. We will explore that use case in Step Four. Another use case, specifically for the profile measure and business measure, is creating a measure entity that is composed of multiple entities. We will explore that use case in Step Five.

In order to choose additional entities, select **Add new entity** and pick the entities of your interest.

> [!div class="mx-imgBorder"] 
> ![](media/select-an-entity.png "Select an entity")

**Note**: You can only select entities which have relationships to your Starting Entity. If you haven't defined relationships yet, see the **Relationships** section.

## Step Four: Calculate a variable

> [!div class="mx-imgBorder"] 
> ![](media/accounts-dynamics-365.png "Accounts Dynamics365")

Select **Add new variable** to open the **Variable Definition** panel.

> [!div class="mx-imgBorder"] 
> ![](media/new-variable-name.png "New variable name")

Let's explore the steps you should complete in this panel.

1. Give your variable a recognizable name. 
2. Select the **Expression** area.
3. Choose a field from the fields shown to the right.
4. Type an expression in the **Expression** area while choosing more fields. **Note**: Currently, we only support arithmetic expressions.
5. Select **Done**.

In the example below, we have defined a calculation for the relative contribution of a single Purchase to the Customer Lifetime Value (CLTV).

> [!div class="mx-imgBorder"] 
> ![](media/new-variable-name2.png "New variable name")


## Step Five: Define your measure entity/attribute

In this step, you will decide how to aggregate your chosen entities and calculations into a measure entity or attribute which you can start using in **Home page**, **Segments**, or any other page. 

**Step 1:** Define first dimension

You can think of a dimension as a *Group by* function. The data within your new Measures entity or attribute will be grouped by all of your defined dimensions. 

In the example below, we have defined **State** as the dimension field of our Measures entity. Upon visiting the Measures entity we have just created on the **Entities** page, we can see that the data we included in that entity (columns shown in blue) is grouped by the *State* column (shown in red).

> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-data-tab.png "Entity grouped by State")

These are the selections you should fill in as part of your dimension's definition (exploring left to right).

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition2.png "Measure definition")

**Entity/variable**: If you define a Measures entity, it should include at least one attribute. If you define a Measures attribute, it will include only one attribute by default. This selection is about choosing the entity that includes that attribute.
**Field**: Here you should pick the specific attribute to be included either in your Measures entity or attribute.
**Bucket**: This is a required selection only if you have selected a **Date** type of attribute. Under this selection, you should decide whether you wish to aggregate the data on a daily, monthly or annual basis.

> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-measure-definition2.png "Text")

**As**: Here you should define the name of your new field in the Measures entity or attribute.
**Display Name**: Here you should define the display name of your field in the Measures entity or attribute. This name will show up both in the customer tile on the **Profiles** page, and within the Customer Card.

**Step 2 (optional)**: Add more dimensions by selecting **Add new dimension** and making the same selections we have just went through.

> [!div class="mx-imgBorder"] 
> ![](media/new-dimension.png "New dimension")

**Step 3 (optional)**: Add measures

This option should be used in case you wish to include aggregated column/s in your Measures entity or attribute. By aggregated column we refer to a column where every value results from a specific calculation being made on one of your original entity's columns. 

For example, let us assume we have added three additional measures: LTV, Purchase Amount, and Service Amount. Each of these three measures represents a summation of other attributes we have in one or more of our ingested entities.

Upon visiting the **Entities** page and choosing the new Measure we have just created, we can see that these three new fields are included in our Measure (shown in blue). Again, these fields' values result from the summation of other attributes. 

> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-data-tab.png "Text")

Let's explore how to add a new measure.

First, select **New Measure**.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition3.png "Measure definition")

Then, make those selections (exploring left to right).

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition4.png "Measure definition")

**Function**: At present, we support **Sum, Min, Max, Count and Unique Count** as aggregation options.
**Entity/Variable**: Here you should choose the entity that includes the attribute on which you wish to base your calculation. You can also choose a *Variable* if you created one as part of step four above. 
**Field**: Pick the specific attribute or variable on which you wish to base your calculation.
**As**: Your calculation will result in a new field. Define the name of your new field in the Measures entity/attribute.
**Display Name**: Define the display name of your new field in the Measures entity/attribute. That name will show up both in the customer tiles within the **Profiles** page and in the Customer Card.

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

Here is an example of the **Re-name measures** window.

> [!div class="mx-imgBorder"] 
> ![](media/rename-measure.png "Rename measure")

## Next Step
Make sure to visit the **Configure Data** section if you haven't completed yet the data configuration process. Otherwise, you may want to utilize the measure you have just created to create your first customers' segment using the **Segments** page. You can also unlock more insights via the **Activities** and **Enrich Profiles** pages.

