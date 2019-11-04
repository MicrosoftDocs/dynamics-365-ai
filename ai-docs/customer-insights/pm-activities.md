---
title: "Activities | MicrosoftDocs"
description: Work with the Activities page in Dynamics 365 Customer Insights
ms.date: 11/04/2019
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
author: m-hartmann
ms.author: mhart
manager: shellyha
---
# Activities

The Activities capability helps consolidate customer activities from various data sources. This creates a customer timeline view. Business analysts can configure activities to be displayed on a customer dashboard with a timeline view, which can be embedded in business applications.

The Activities capability includes two components:
- **Activities** page: Access this from the **Activities** tab on the left-side menu. Use it to define the activities that you want to view on the customer’s timeline grid.
- **Timeline grid**: This grid consolidates all the activities of one customer in chronological order, and it can be viewed either within model-driven apps in Dynamics 365 (such as Dynamics 365 Sales and Dynamics 365 Customer Service), via the Customer Card add-in, or within a Power BI dashboard. A specific control is used for the creation of that grid. Visit the [**Timeline Control** subsection](pm-customer-card-addin.md#timeline-control) within the **Customer Card Add-In** section to learn how to work with that control.

This topic covers only the **Activities** page.

## Define an activity

Your data sources include entities with transactional and activity data from multiple data sources. On this page, you will identify these entities and select the activities you want to view on the customer’s timeline grid. Choose the entity that includes your target activity or activities.

1. Select **Add activity**.
  
   > [!div class="mx-imgBorder"] 
   > ![Activities add entity](media/activities-add-entity.png "Activities add entity")

> [!NOTE]
> To be included in the timeline grid, an entity must have at least one attribute of type **Date**. Entities without **Date** fields will not be added. If no such entity is identified, the **Add activity** control is disabled.

2. Provide values for the following fields.

    -	**Select entity**: Select an entity that includes transactional or activity data. 
    -	**Primary key**: Use this field to distinguish between all of your entity's records. This field should not contain any duplicate values, null values, or missing values.
    - **Activity name**: Give your activity a recognizable name.
    -	**Activity time**: Select the field that represents the start time of your activity.
    -	**Description** (not mandatory): Select the field that represents a description of the activity

3. Set up a relationship.

   > [!div class="mx-imgBorder"] 
   > ![Define the entity relationship](media/activities-entities-define.png "Define the entity relationship")

    - **Source field**: Select the field in your activity entity that will be used to establish a relationship with another entity.
    - **Target entity**: Select the entity with which your Activity entity will be in relationship.
    -	**Target field**: Select the field in the Target entity that will be used to establish a relationship with the Activity entity.

4. Select **Done** to save your selections. Then, select **Run** on the **Activities**.

   
## Next steps

Once you define your activities, you can:
1. Explore the [**Timeline Control** subsection](pm-customer-card-addin.md#timeline-control) under the **Customer Card Add-in** section in order to learn how to view information on these activities for each of your customers.
2. Visit the **Connectors** section to learn how to set up the **Power BI** dashboard where you can also view information on these activities for each of your customers.

