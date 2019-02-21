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

The **Measures page** enables you to define all the KPIs that best reflect your specific business performance and health. It can either be customer related measures such as *Lifetime Value*, or business health measures such as *Monthly Active Users*. Customer Insights provides an intuitive experience to build different types of measures, with a query builder wizard that doesn’t require the user to manually code or validate the query. 

Once defined, you can benefit from your measures in a variety of ways. For example:

- Track your business health measures on your **Home page**
- View customer measures for a specific customer as part of the **Customer Card**. See the **Customer Card Add-in section** to learn more.
- Use to define a customer segment, using the **Segment Builder page.** See the **Segments section** to learn more.

## Step One: Choose between three measure types

Customer Insights supports 3 types of measures:

- **Profile Attribute**: this measure represents is a single value per customer, that reflects a score, value or state for the customer. Profile attributes are created as attributes in a new system generated entity called **Customr_Measure.** Examples: *Lifetime Value,* *Total Sales* etc.

> [!div class="mx-imgBorder"] 
> ![](media/measures-customer-entity.png "Customer_Measure attribute")

- **Profile Measure**: This measure provides input on customer behavior with breakdown by dimensions. A new entity will be generated per measure, with potential multiple records per customer. Examples: *Number of visits per channel*, *Total sales per day*
- **Business Measure**: This measure helps you track your business performance and health. A new entity will be generated per measure. Examples: *Average sales per customer*, *MAU*

You will first select the type of measure when clicking on New Measure:

There are two early decisions you should make with regard to your desired measure. These decisions will help you choose between the three options that are available to you upon selecting **New Measure**.

> [!div class="mx-imgBorder"] 
> ![](media/search-measures.png "Search measures")

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

Customer Insights lets you build measures leveraging data from multiple data sources, that are now connected through the *Customer entity*. At this point you should decide whether additional entities are needed as part of your measure definition. One use case might be creating an expression that will be based on attributes from two or more different entities. We will explore that use case in Step Four. Another use case, specifically for the profile measure and business measure, is creating a measure entity that is composed of multiple entities. We will explore that use case in Step Five.

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

In this step, you will decide how to aggregate and summarize your chosen entities and calculated variables into a measure entity or attribute. 

**Step 1: Defining first dimension**

What is a dimension? You can think of a dimension as a **Group by** function: The data within your new Measures entity or attribute will be grouped by all of your defined dimensions.

In the example below, we have defined **State** as the dimension field of our **BusinessReport: Customer 360** Measures entity. Upon visiting the Measures entity we have just created on the **Entities screen**, we can see that the data we included in that entity (columns shown in blue) is grouped by the State column (as shown in red):

> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-data-tab.png "Entity grouped by State")

These are the selections you should fill in as part of your dimension's definition (exploring left to right).

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition2.png "Measure definition")

**Entity/variable**: If you define a Measures entity, it should include at least one attribute. If you define a Measures attribute, it will include only one attribute by default. This selection is about choosing the entity that includes that attribute. <br />
**Field**: Here you should pick the specific attribute to be included either in your Measures entity or attribute. <br />
**Bucket**: This is a required selection only if you have selected a **Date** type of attribute. Under this selection, you should decide whether you wish to aggregate the data on a daily, monthly or annual basis.

> [!div class="mx-imgBorder"] 
> ![](media/measures-businessreport-measure-definition2.png "Text")

**As**: Here you should define the name of your new field in the Measures entity or attribute. <br />
**Display Name**: Here you should define the display name of your field in the Measures entity or attribute. This name will show up both in the customer tile on the **Profiles** page, and within the Customer Card.

**Step 2 (optional)**: Add more dimensions by selecting **Add new dimension** and making the same selections we have just went through.

> [!div class="mx-imgBorder"] 
> ![](media/new-dimension.png "New dimension")

**Step 3 (optional)**: Add aggragate functions 

You can use previously defined measures as building blocks for your aggregations. Any aggragation that you will create will result in a new field within your Measures entity or attribute. 

Supported aggragation functions at this point are: **Min, Max, Average, Median, Sum, and Count Unique.**

For example, let us assume we have added the following aggragated field: **Average Service Amount** that takes the average of every **Service Amount** field within the entity **Service: Orders** and averages it:

// 1

Upon visiting the **Entities** page and choosing the new Measure we have just created (called **Aggragated Example**), we can see that our aggragation formula had created the new field **Average Service Amount**:

// 2

Let's explore the steps involved in defining a new measure.

First, select **New Measure**.

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition3.png "Measure definition")

Then, make those selections (exploring left to right).

> [!div class="mx-imgBorder"] 
> ![](media/measure-definition4.png "Measure definition")

**Function**: At present, we support **Sum, Min, Max, Count and Unique Count** as aggregation options. <br />
**Entity/Variable**: Here you should choose the entity that includes the attribute on which you wish to base your calculation. You can also choose a *Variable* if you created one as part of Step Four above. <br />
**Field**: Pick the specific attribute or variable on which you wish to base your calculation. <br />
**As**: Your calculation will result in a new field. Define the name of your new field in the Measures entity/attribute. <br />
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

