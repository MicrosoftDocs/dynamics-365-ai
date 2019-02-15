---
title: "Data Sources | MicrosoftDocs"
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
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# Data Sources

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

You can bring in data to Customer Insights by using the 20+ out-of-the-box connectors that we make available for sources such as Customer Engagement, SQL Azure, and Blob store. Even if you don’t find a suitable out-of-the-box connector for your source, you can always export the data from your source as a CSV file and import to Customer Insights using our CSV connector. To import data to Customer Insights, you need to create a data source in the **Data Sources** page. It’s recommended to have multiple data sources as it will allow you to have different refresh schedules and credentials for each of your data sources.

## Bring your data into Customer Insights 

> [!IMPORTANT]
> Currently, on-premises data sources are not supported in Customer Insights. 

### Step One (mandatory): Creating a new data source on the Data Sources page

To load data to Customer Insights, follow the following process:

1. Navigate to **Data Sources** from the **Data Manager** page.

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-tile.png "Get data tile")

2. Select **Get data**.

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-add.png "Get data add")

3. Provide a name for the data source and select **Save**. This will create the data source for you. 

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-create.png "Get data create")

4. Pick one of the many available connectors that are available in the screen below.

   - Some of the following data sources are not yet supported, such as OData. 

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-select-source.png "Get data select source")

   - If you wish to load data from Customer Engagement, choose the  **Common Data Service for Apps** connector.

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-connection-settings.png "Get data connection settings")
   
   - Note that some of the following connectors replaced older connector versions. For example, if you wish to utilize the Dynamics 365 AX connector, you should choose the **Common Data Service for Apps** option.

5. After choosing a connector, you will be required to fill in some fields. For further guidance around filling in those fields for some of the most common data sources (Dynamics 365, CSV and text files, Blob storage, Azure SQL Database, etc), review [Common Connectors Guidance](pm-common-connectors.md).  

### Step Two (mandatory): Adding and reviewing entities

In the this step, you'll add entities to your data source. In Customer Insights, entities are datasets. For example, If you have a database that includes multiple datasets, each of those datasets is an entity (an Orders dataset, a Sales dataset, etc.). 

1. Use the power query window shown below to review and possibly configure the data. The entities that the system identified in your selected datasource will appear on the left (shown in red).

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-configure-edit-queries.png "Edit queries")
   
You can add additional entities to your data source by selecting **Get Data**.

// 1

2. In this step you can also edit and transform the data. First, choose an entity to edit or transform and then use one of the menus located at top of the Power Query window to find a specific transformation (those are shown in blue above). Also, note that after selecting each transformation, it will be added as a processing step. You can view and remove steps in the part shown in green above. Exploring how your data looks like after a specific subset of added steps can be done by selecting the final step in that subset.

   Optionally, to avoid data-related issues, you should complete the next few transformations.

   - If you are ingesting data from a CSV file and the first row has headers, you should open the **Transform Table** menu and then select the **Use headers as first row** option.

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-transform-table.png "Get data transform table")

   - In addition, it is recommended to map your data to standard format of data. Customer Insights allows you to map your data to the Microsoft Common Data Model (CDM). In order to do so, select **Map to Standard**, and then map fields from your source data to CDM fields.

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-map-entity.png "Map to standard entity")

3. Select **Create** at the bottom of the power query screen to save.

   > [!div class="mx-imgBorder"] 
   > ![](media/configure-data-edit-queries-create.png "Create")

4. After saving, you can expect to see your datasource added in the **Data Sources** page:

   > [!div class="mx-imgBorder"] 
   > ![](media/configure-data-datasource-added.png "Datasource added")

For each of your ingested datasources, besides its name, you can expect to see the last time the data was refreshed for that datasource, as well as its status. There are three possible status: 
1. Data was successfully ingested (example is shown in blue in the image above)
2. No data was ingested yet (example is shown in red in the image above)
3. Data is still loading into Customer Insights (represented by a *warning sign* icon)

At this point you should refresh the datasource that you just saved. Select the button highlighted below in red and then select **Refresh** as highlighted in blue:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-sources-refresh.png "Data sources refresh")

At this point, repeat the same steps for each datasource you wish to ingest into Customer Insights.

### Step Three (optional): Reviewing Ingested Data

It is possible that the data load will take some time. After successfully refreshing, the ingested data can be reviewed from the **Entities page** as shown below. For more information on the **Entity** page see [!INCLUDE [pm-entities](pm-entities.md)].

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-data.png "Data manager entities")

### Step Four (optional) Editing existing data sources

> [!NOTE]
> The Edit operation is only available for data sources that are not currently refreshing.

Follow these steps to edit an existing data source. 

1. Browse to the data source that you wish to edit:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-source.png "Get data source")

2. Click on the **Edit** button to edit the data source in Power Query: 

   > [!div class="mx-imgBorder"] 
   > ![](media/configure-data-sources-edit2.png "Edit data source")

3. Don't forget to hit **Create** in the Power Query screen upon completing the edits in order to save your changes. If you wish to remove a data source, click **Delete** for that data source:

   > [!div class="mx-imgBorder"] 
   > ![](media/configure-data-sources-delete.png "Data sources delete")

### Next steps:
At this point you are ready to unlock unique customer insights through the mandatory **Configure Data** sections (those include **Map**,**Match** and **Merge**). If you first wish to review all the entities that were ingested, visit the **Entities** section first. 

