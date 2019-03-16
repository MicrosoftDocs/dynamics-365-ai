---
title: "Measures | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/13/2019
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

The **Measures** page enables you to define all the key performance indicators (KPIs) that best reflect your specific business performance and health. It can either be customer-related measures such as *Lifetime Value* or business-health measures such as *Monthly Active Users*. Customer Insights provides an intuitive experience to build different types of measures, with a query-builder wizard that doesn’t require the user to manually code or validate the query. 

Once defined, you can benefit from your measures in a variety of ways. For example:

- Track your business measures on your **Home** page.
- View customer measures for a specific customer as part of the **Customer Card**. See the **Customer Card Add-in section** to learn more.
- Use to define a customer segment using the **Segment Builder** page. See the **Segments section** to learn more.

## Step One: Choose between three measure types

Customer Insights supports three types of measures:

- **Customer Attribute**: This measure is a single value per customer that reflects a score, value, or state for the customer. Profile attributes are created as attributes in a new system-generated entity called **Customr_Measure.** Examples are *Lifetime Value* and *Total Sales*.

> [!div class="mx-imgBorder"] 
> ![](media/measures-customer-entity.png "Customer_Measure attribute")

- **Customer Measure**: This measure provides input on customer behavior with breakdown by dimensions. A new entity will be generated per measure, with potential multiple records per customer. Examples: *Number of visits per channel* and *Total sales per day*.
- **Business Measure**: This measure helps you track your business performance and health. Examples: *Average sales per customer* and *MAU*.

Note that there are two possible outputs for the business measure:
    -1. A single-number measure that will show up on the Home page
    -2. A new entity
Later we will show how to create both of these options.

You will first select the type of measure when you select **New Measure**:

> [!div class="mx-imgBorder"] 
> ![](media/search-measures.png "Search measures")

## Step Two: Choose the starting entity

Upon selecting **New Measure**, you will get to the **Measure Creation** panel. For example, after selecting the **Business Measure** option, you will see the following:

> [!div class="mx-imgBorder"] 
> ![](media/new-business-measure.png "New business measure")

- **Name** (mandatory): After completing the configuration of your measure, it will show up in the **Measures** page under this name.
- **Display name** (optional): As mentioned earlier, your measure will also be added as an attribute or be saved as a new entity. In both cases, the measure will carry the Display Name in the Home page, Customer Card, etc.
- **Starting entity** (mandatory): Here, you should choose the entity on the basis of which you wish to construct your measure. If you wish to include fields from multiple entities in your measure fields, choose any of these entities.  

Here is the panel you will see upon selecting the **Customer Measure** option:

> [!div class="mx-imgBorder"] 
> ![](media/new-profile-measure.png "New profile measure")

This panel is the same panel we explored under the previous option, except for one difference: The Customer Profile entity will automatically be selected as your starting entity. This default selection can't be changed.

Finally, here is the panel you will see upon selecting the **Customer Attribute** option:

> [!div class="mx-imgBorder"] 
> ![](media/new-profile-attribute.png "New profile attribute")

## Step Three: Choose related entities

After completing Step Two, you'll see the following page:

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition.png "Measure definition")

Customer Insights lets you build measures leveraging data from multiple data sources that are now connected through the Customer entity. At this point, you should decide whether additional entities are needed as part of your measure definition. One use case might be creating an expression that will be based on attributes from two or more different entities. We will explore that use case in Step Four. Another use case, specifically for the customer measure and business measure, is creating a measure entity that is composed of multiple entities. We will explore that use case in Step Five.

In order to choose additional entities, select **Add new entity**, and choose the entities you want.

> [!div class="mx-imgBorder"] 
> ![](media/select-an-entity.png "Select an entity")

**Note**: You can only select entities that have relationships to your starting entity. If you haven't defined relationships yet, see the **Relationships** section.

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
4. Type an expression in the **Expression** area while choosing more fields. **Note**: Currently, we support arithmetic expressions only.
5. Select **Done**.

In the following example, we have defined a calculation for the relative contribution of a single purchase to the Customer Lifetime Value (CLTV).

> [!div class="mx-imgBorder"] 
> ![](media/new-variable-name2.png "New variable name")

## Step Five: Define your measure entity/attribute

In this step, you will decide how to aggregate and summarize your chosen entities and calculated variables into a Measures entity or attribute. 

**Step 1: Defining first dimension**

What is a dimension? You can think of a dimension as a **Group by** function: The data within your new Measures entity or attribute will be grouped by all of your defined dimensions.

In the example below, we have defined **State** as the dimension field of our **BusinessReport: Customer 360** Measures entity. Upon visiting the Measures entity that we have just created on the **Entities** screen, we can see that the data we included in that entity (columns shown in blue) is grouped by the State column (as shown in red).

// 1
> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-data-tab.png "Entity grouped by State")

These are the selections you should fill in as part of your dimension's definition:

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition2.png "Measure definition")

**Entity/variable**: If you define a Measures entity, it should include at least one attribute. If you define a Measures attribute, it will include only one attribute by default. This selection is about choosing the entity that includes that attribute. <br />
**Field**: Here you should pick the specific attribute to be included either in your Measures entity or attribute. <br />
**Bucket**: This is a required selection only if you have selected a **Date** type of attribute. Under this selection, you should decide whether you want to aggregate the data on a daily, monthly, or annual basis.

> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-measure-definition2.png "Measure definition")

**As**: Here you should define the name of your new field in the Measures entity or attribute. <br />
**Display Name**: Here you should define the display name of your field in the Measures entity or attribute

**Note**: When it comes specifically to the **Business measure**, your measure will be saved as a single-number entity and will show up in the Home page unless you complete Step 2 below (adding more dimensions to your measure). If you complete Step 2, the measure will **not** show up on the **Home** page.

**Step 2 (optional)**: Add more dimensions by selecting **Add new dimension** and making the same selections we have just gone through.

> [!div class="mx-imgBorder"] 
> ![](media/new-dimension.png "New dimension")

**Step 3 (optional)**: Add aggregate functions 

Any aggregation that you create will result in a new value within your Measures entity or attribute. 

Supported aggregation functions are: **Min**, **Max**, **Average**, **Median**, **Sum**, and **Count Unique**.

For example, let's assume that we have added the aggregated value **Average Service Amount**, which takes the average of every **Service Amount** field within the entity **Service: Orders** and averages it:

> [!div class="mx-imgBorder"] 
> ![](media/measures-aggregated-field-example.png "Aggregated field example")

Upon visiting the **Entities** page and choosing the new measure we have just created (called **Aggregated Example**), we can see that our aggregation formula has created the new value **Average Service Amount**.

> [!div class="mx-imgBorder"] 
> ![](media/measures-aggregated-field-example2.png "Aggregated field example")

Let's explore the steps involved in defining a new value.

<!--note from editor: screen shots at lines 170 and 175 look identical except for the blue outlining  -->

First, select **New value**.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition3.png "Measure definition")

Then, make your selections.

// 4 <!-- no need to add any highlighting. Just replace-->
> [!div class="mx-imgBorder"] 
> ![](media/measure-definition4.png "Measure definition")

**Function**: At present, we support **Sum**, **Min**, **Max**, **Count** and **Unique Count** as aggregation options. <br />
**Entity/Variable**: Here you should choose the entity that includes the attribute on which you wish to base your calculation. You can also choose a variable if you created one as part of Step Four. <br />
**Field**: Pick the specific attribute or variable on which you wish to base your calculation. <br />
**As**: Your calculation will result in a new value. Define the name of your new value in the Measures entity/attribute. <br />
**Display Name**: Define the display name of your new value in the Measures entity/attribute

Save your measure.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition-save.png "Measure definition")

## View and edit your measures 

Once you have completed your first measure, you'll see the following page summarizing your created measures.

> [!div class="mx-imgBorder"] 
> ![](media/new-measure.png "New measure")


<!--note from editor:Confused about what sentence below refers to: is it referencing line 167, "First, select **New Measure**"?   -->

At any time, you can create a new measure via **Add Measure** shown earlier.

<!--note from editor: in sentence below, change "following button" to "**Measure menu** button"?   -->

You can also edit, delete or rename the data of any of your created measures by first selecting the following button.

> [!div class="mx-imgBorder"] 
> ![](media/measure-menu.png "Measure menu")

Choose from the **Options** drop-down menu.

> [!div class="mx-imgBorder"] 
> ![](media/measure-menu2.png "Measure menu")

Here is an example of the **Rename measures** window.

> [!div class="mx-imgBorder"] 
> ![](media/rename-measure.png "Rename measure")

## Next Step
Make sure to visit the **Unify** section if you haven't yet completed the data configuration process. Upon the completion of the Unify modules, you might want to use the measure you have just created to create your first customers' segment using the **Segments** page. You can also unlock more insights via the **Activities** and **Enrich Profiles** pages.

