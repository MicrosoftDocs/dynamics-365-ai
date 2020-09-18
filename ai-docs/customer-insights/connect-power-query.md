---
title: "Available data sources for Dynamics 365 Customer Insights | Microsoft Docs"
description: "Inbound connectors for data sources in Dynamics 365 Customer Insights."
ms.date: 03/20/2020
ms.reviewer: adkuppa
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Connect to a Power Query data source

Adding data sources based on Power Query connectors usually follow the same steps as outlined below.
## Create a new data source

1. In Customer Insights, go to **Data sources**.

2. Select **Get data**.

3. Provide a **Name** for the data source, and select **Save** to create the data source.

4. Choose one of the available connectors. To load data from Dynamics 365 apps, choose the **Common Data Service** connector.

5. Enter the required details for the selected connector.

## Available Power Query data sources

See the [Power Query connector reference](https://docs.microsoft.com/power-query/connectors/) for an up-to-date list of connectors that you can select to import data to Customer Insights. 

All connectors that have a checkmark in the **Customer Insights (Dataflows)** column are available when creating a new data source in Customer Insights. Have a look at the connector reference of a specific connector to learn more about its prerequisites and other details.

## Edit Power Query data sources

> [!NOTE]
> You can only edit data sources that aren't in the process of refreshing.

1. In Customer Insights, go to **Data sources**.

2. Select the vertical ellipsis next to the data source you want to change and select **Edit** from the drop-down menu.

<Screenshot>

3. Apply your changes in the **Edit queries** Power Query dialog.

4. Select **Create** in Power Query after completing your edits to save your changes.

### Add, review, and transform entities

In this step, you'll add entities to your data source. In Customer Insights, entities are datasets. If you have a database that includes multiple datasets, each dataset is its own entity.

1. In the **Edit queries** dialog of Power Query you can review and refine the data. The entities that the systems identified in your selected data source appear in the left pane (1).

   > [!div class="mx-imgBorder"]
   > ![Edit queries dialog with three areas highlighted](media/data-manager-configure-edit-queries.png "Edit queries dialog with three areas highlighted")

2. You can also transform your data. Select an entity to edit or transform. Then, open one of the menus (2) located at the top of the Power Query window to find a specific transformation. Each transformation is added as a processing step (3), which can be modified as needed.

   > [!NOTE]
   > It might not be possible to make changes to data sources that are currently being used in one of the app's processes (*segmentation*, *match*, or *merge*, for example). Using the **Settings** page, you can track the progress of each of the active processes. When a process completes, you can return to the **Data Sources** page and make your changes.

3. You can add additional entities to your data source by selecting **Get data** in the **Edit queries** dialog.

   These transformations are highly recommended:

   - If you're ingesting data from a CSV file, and the first row has headers, go to **Transform table** and select **Use headers as first row**.

   - Map your data to a standard format of data. Customer Insights allows you to map your data to the Common Data Model. To do so, select **Map to standard** in the Power Query header, and then map fields from your source data to Common Data Model fields.

4. Select **Create** at the bottom of the Power Query window to save the transformations. After saving, you'll find your data source on the **Data sources** page.

5. On the **Data sources** page, select the ellipsis under **Actions** and then select **Refresh**.

> [!TIP]
> Power Query provides a lot of pre-built transformation options. For more information, see [Power Query Transformations](https://docs.microsoft.com/power-query/power-query-what-is-power-query#transformations).
