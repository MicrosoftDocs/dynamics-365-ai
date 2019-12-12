---
title: "Measures in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Define customer-related measures to analyze and reflect the performance of certain business areas."
ms.date: 12/04/2019
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
ms.reviewer: nimagen
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

6. Optionally, you can configure variables. In the **Variables** section, select **New variable**.

   Variables are calculations that are made on each of your selected records. For example, summing point-of-sale (POS) and online sales for each of your customers' records.

7. Provide a **Name** for the variable.

8. In the **Expression** area, choose a field to begin your calculation with.

9. Type an expression in the **Expression** area while choosing more fields to be included in your calculation.

   > [!NOTE]
   > Currently, Customer Insights supports arithmetic expressions only. Additionally, variable calculation isn't supported for entities from different [entity paths](pm-relationships.md).

10. Select **Done**.

11. In the **Measure definition** section, you'll define how your chosen entities and calculated variables are aggregated in a new measure entity or attribute.

12. Select **New dimension**. You can think of a dimension as a *group by* function. The data output of your Measure entity or attribute will be grouped by all of your defined dimensions.

    > [!div class="mx-imgBorder"]
    > ![Choose aggregate cycle](media/measures-businessreport-measure-definition2.png "Choose aggregate cycle")

    Select or enter the following information as part of your dimension's definition:

    - **Entity**: If you define a Measure entity, it should include at least one attribute. If you define a Measure attribute, it will include only one attribute by default. This selection is about choosing the entity that includes that attribute.
    - **Field**: Choose the specific attribute to be included either in your Measure entity or attribute.
    - **Bucket**: Choose whether you want to aggregate data on a daily, monthly, or annual basis. This is a required selection only if you have selected a Date type attribute.
    - **As**: Defines the name of your new field.
    - **Display name**: Defines the display name of your field.

    > [!NOTE]
    > Your business measure will be saved as a single-number entity and will appear on the **Home** page unless you add more dimensions to your measure. After adding more dimensions, the measure will *not* show up on the **Home** page.

13. Optionally, add aggregation functions. Any aggregation that you create results in a new value within your Measures entity or attribute. Supported aggregation functions are: **Min**, **Max**, **Average**, **Median**, **Sum**, **Count Unique**, **First** (takes the first record of a dimension value), and **Last** (takes the last record that was added to a dimension value).

14. Select **Save** to apply your changes to the measure.

## View your measures

After creating at least one measure, you'll see a list of measures on the **Measures** page in Customer Insights.

You'll find information about the measure type, the creator, creation date and time, last edit date and time, status (whether the measure is active, inactive or failed from being created), and last refresh date and time. When you select a measure from the list, you can see a preview of the measure output.

To export the data, select **Download as CSV** after opening the measure preview.

## Edit measures

<!-- add screenshot showing the ellipsis -->

You can edit or rename your created measures.

1. Go to the **Measures** page.

2. Select the vertical ellipsis next to the measure you want to change.

3. Choose **Edit** from the options in the drop-down menu.

4. Apply your changes and select **Save**.

## Delete measures

You can delete existing measures.

1. Go to the **Measures** page.

2. Select the vertical ellipsis next to the measure you want to delete.

3. Choose **Delete** from the options in the drop-down menu.

4. Confirm your deletion.

## Next step

You cam use existing measures to create your first customer segment on the **Segments** page. For more information, see [Segments](pm-segments.md).
