---
title: "Activities | Microsoft Docs"
description: "Define activities in Dynamics 365 Customer Insights to see them in a customer timeline." 
ms.date: 04/06/2020
ms.service: dynamics-365-ai
ms.reviewer: mukeshpo
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Activities

Combine customer activities from various data sources in Dynamics 365 Customer Insights. In a next step, create a customer timeline that includes all the activities of a customer in chronological order. You can include the timeline in model-driven apps in Dynamics 365 via the Customer Card add-in, or in a Power BI dashboard. Visit the [**Timeline Control** section](pm-customer-card-addin.md#timeline-control) to learn how to configure that control.

This article covers only the **Activities** page.

## Define an activity

Your data sources include entities with transactional and activity data from multiple data sources. Identify these entities and select the activities you want to view on the customer's timeline. Choose the entity that includes your target activity or activities.

1. In Customer Insights, go to **Data** > **Activities**.

1. Select **Add activity**.

   > [!NOTE]
   > An entity must have at least one attribute of type **Date** to be included in a customer timeline and you can't add entities without **Date** fields. The **Add activity** control is disabled if no such entity is found.

1. In the **Add activity** pane, set the values for the following fields:

   - **Entity**: Select an entity that includes transactional or activity data.
   - **Primary key**: Select the field that uniquely identifies a record. It shouldn't contain any duplicate values, empty values, or missing values.
   - **Timestamp**: Select the field that represents the start time of your activity.
   - **Event**: Select the field that is the event for the activity.
   - **Details**: Optionally, select the field that is added for additional details.
   - **Icon**: Optionally, select the icon that represents this activity.

1. In the **Set up relationship** section, configure the details to connect your activity data to its corresponding customer.

   > [!div class="mx-imgBorder"]
   > ![Define the entity relationship](media/activities-entities-define.png "Define the entity relationship")

    - **Activity entity field**: Select the field in your activity entity that will be used to establish a relationship with another entity.
    - **Customer entity**: Select the corresponding source customer entity with which your activity entity will be in relationship. You can relate to only those source customer entities that are used in the data unification process.
    - **Customer entity field**: This field shows the primary key of the source customer entity as selected in the map process. This primary key field in the source customer entity is used to establish a relationship with the activity entity.
    - **Name**: If a relationship between this activity entity and the selected source customer entity already exists, the relationship name will be in read-only mode. If there no such relationship exists, a new relationship will be created with the name provided here.

1. Select **Save** to apply your changes.

1. On the **Activities** page, select **Run**.

## Edit an activity

1. In Customer Insights, go to **Data** > **Activities**.

2. Select the activity entity you want to edit and select **Edit**. r, you can hover over the entity row and select the **Edit** icon.

3. Click on the **Edit** icon.

4. In the **Edit activity** pane, update the values and select **Save**.

5. On the **Activities** page, select **Run**.

## Delete an activity

1. In Customer Insights, go to **Data** > **Activities**.

2. Select the activity entity you want to remove and select **Delete**. Or, you can hover over the entity row and select the **Delete** icon. Additionally, you can select multiple activity entities to be deleted at once.
   > [!div class="mx-imgBorder"]
   > ![Edit or delete the entity relationship](media/activities-entities-edit-delete.png "Edit or delete the entity relationship")

3. Select on the **Delete** icon.

4. Confirm your deletion.

## Next steps

You can review the [Customer Card add-in](pm-customer-card-addin.md) article to show activities in model-driven apps. To build a Power BI dashboard, have a look at the [Power BI connector](pm-connectors.md) article.
