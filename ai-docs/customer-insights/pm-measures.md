---
title: "Measures in Dynamics 365 Customer Insights | Microsoft Docs"
description: Define customer-related measures to analyze and reflect the performance of certain business areas. 
ms.date: 11/20/2019
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
---
# Measures

**Measures** represent key performance indicators (KPIs) that reflect the performance and health of specific business areas. Dynamics 365 Customer Insights provides an intuitive experience for building different types of measures, using a query-builder that doesn’t require you to manually code or validate your measures. You can track your business measures on the **Home** page, see measures for a specific customer as part of the **Customer Card**, and use measures to define a customer segments on the **Segments** page.

[View this video - Getting Started: Creating Customer and Business Measures](https://youtu.be/aSM1YV84KUc).

## Create a measure

This section walks you through on creating a measure from scratch. You can build measures by leveraging data from multiple data sources that are connected through the Customer entity

1. In Customer Insights, go to **Measures**.

2. Select **New measure**.

3. Choose the measure **Type**:
 
   - **Customer attribute**: A single field per customer that reflects a score, value, or state for the customer. Customer attributes are created as attributes in a new system-generated entity called **Customer_Measure**.

   - **Customer measure**: Insights on customer behavior with breakdown by selected dimensions. A new entity is generated for each measure, potentially with multiple records per customer.

   - **Business measure**: Tracks your business performance and health of the business. Business measures can have two different outputs: a numeric output that shows on the **Home** page or a new entity that you find on the **Entities** page.

4. Provide a **Name** and an optional **Display name**, then select **Next**.

5. In the **Entities** section, select the first entity from the drop-down list. At this point, you should decide whether additional entities are needed as part of your measure definition.

   > [!div class="mx-imgBorder"] 
   > ![Measure definition](media/measure-definition.png "Measure definition")

   To add more entities, select **Add entity** and select entities you want to use for the measure.

   > [!NOTE]
   > You can select only entities that have relationships to your starting entity. If you haven't defined relationships yet, see [Relationships](pm-relationships.md) for more details.

6. In the **Variables** section, select **New variable**.

   Variables are calculations that are made on each of your selected records. For example, summing point-of-sale (POS) and online sales for each of your customers' records.

7. Provide a **Name** for the variable.

<!---->

8. Select the **Expression** area.
3. Choose a field from the list of fields to the right of the **Expression** area to begin your calculation with.
4. Type an expression in the **Expression** area while choosing more fields to be included in your calculation.

   > [!NOTE]
   > Currently, Customer Insights supports arithmetic expressions only. Moreover, at present variable calculation is not supported for entities from different entity-paths (visit the **Relationships** section to learn more about what is considered to be an "entity path").

5. Select **Done**.

In the following example, we have defined a calculation for the relative contribution of a single purchase to the Customer Lifetime Value (CLTV).

## Step 5: Define your Measure entity or attribute

In this step, you will decide how to aggregate and summarize your chosen entities and calculated variables into a Measures entity or attribute. 

**Step 1**: Defining first dimension.

You can think of a dimension as a “group by” function: The data within your new Measure entity or attribute will 
be grouped by all of your defined dimensions.

In the following example, we have defined **State** as the dimension field of the **BusinessReport: Customer 360** Measure entity. On the screen, we can see that the data we included in that entity (first column) is grouped by the State column (second column).

Select or enter the following information as part of your dimension's definition:

> [!div class="mx-imgBorder"] 
> ![Measure definition](media/measure-definition2.png "Measure definition")

**Entity/variable**: If you define a Measure entity, it should include at least one attribute. If you define a Measure attribute, it will include only one attribute by default. This selection is about choosing the entity that includes that attribute. <br />
**Field**: Choose the specific attribute to be included either in your Measure entity or attribute. <br />
**Bucket**: Choose whether you want to aggregate data on a daily, monthly, or annual basis. This is a required selection only if you have selected a Date type of attribute. 

> [!div class="mx-imgBorder"] 
> ![Choose aggregate cycle](media/measures-businessreport-measure-definition2.png "Choose aggregate cycle")

**As**: Defines the name of your new field in the Measure entity or attribute. <br />
**Display name**: Defines the display name of your field in the Measure entity or attribute.

> [!NOTE]
> Your Business measure will be saved as a single-number entity and will appear on the home page unless you complete Step 2 below (adding more dimensions to your measure). If you complete Step 2, the measure will **not** show up on the home page.
  
**Step 2 (optional)**: Add more dimensions by selecting **Add new dimension** and making the same selections we have just illustrated.

**Step 3 (optional)**: Add aggregate functions. 

Any aggregation that you create results in a new value within your Measures entity or attribute. 
Supported aggregation functions are: **Min**, **Max**, **Average**, **Median**, **Sum**, **Count Unique**, **First**, and **Last**.

Note: 
- Under the **Last** operator, the last record that was added to each dimension value will be taken. For example, if the dimension is CustomerID and the Last operator is applied on a Sales attribute, the result will be the last sales record for each CustomerID.
- Under the **First** operator, the first record will be taken for each dimension value.


For example, let's assume that we have added the aggregated value **Average Service Amount**, which takes the average of every **Service Amount** field within the entity **Service: Orders** and averages it.

When visiting the **Entities** page and choosing the new measure we have just created (called **AggregatedFieldExample**), we can see that our aggregation formula has created the new value **Average Service Amount**.

Let's explore the steps involved in defining a new value.

1. First, select **New value**.

2. Then, make your selections.

   - **Function**: At present, we support **Sum**, **Min**, **Max**, **Count**, and **Unique Count** as aggregation options. <br />
   - **Entity/variable**: Choose the entity that includes the attribute on which you want to base your calculation. You can also choose a variable if you created one as part of Step 4. <br />
   - **Field**: Choose the specific attribute or variable on which you want to base your calculation. <br />
   - **As**: Your calculation will result in a new value. Define the name of your new value in the Measures entity/attribute. <br />
   - **Display name**: Define the display name of your new value in the Measures entity/attribute.

3. Save your measure.

    > [!div class="mx-imgBorder"] 
    > ![Save measure definition](media/measure-definition-save.png "Save measure definition")

## View your measures 

Once you have completed your first measure, you'll see the following page summarizing your created measures.

> [!div class="mx-imgBorder"] 
> ![Summary of new measures](media/new-measure.png "Summary of new measures")

This table lists the measure’s type, creation owner, creation date and time, edit owner, last edit sate and time, status (whether the measure is active, inactive or failed from being created), and last refresh date and time. When you select a measure, you can see a preview of the measure output. Select **Donwnload as CSV** to export the data.

As mentioned before, you can also view your created measure in one of the following ways:
- If you created a **Customer measure**, you can view your new measure entity on the **Entities** page.  
- If you created a **Customer attribute**, you can view your new attribute on the **Entities** page. Look for the *Customer_Measure* entity.
- If you created a **Business measure** with no dimensions, you can view your created measure on the **Home** page (under the *Insights* section). 
- Lastly, if you created a **Business measure** with one or more dimensions, you can find your new measure entity on the **Entities** page. 

## Edit measures

You can also edit, delete, or rename the data of any of your created measures by first selecting the vertical ellipsis.

Choose options from the drop-down menu.

## Delete measures



## Next step
Make sure to visit the **Unify** section if you haven't yet completed the data configuration process. Upon the completion of the Unify modules, you might want to use the measure you have just created to create your first customers segment using the **Segments** page. You can also unlock more insights via the **Activities** and **Enrich Profiles** pages.