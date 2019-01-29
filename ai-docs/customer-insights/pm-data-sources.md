---
title: "Data Sources | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
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
robots: noindex,nofollow
---
# Data Sources

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

**You can bring in data to Customer 360 by using the 20+ out-of-the-box connectors** that we make available for sources, such as Dynamics 365, SQL Azure, and Blob store. Even if you don’t find a suitable out-of-the-box connector for your source, **you can always export the data from your source as a CSV file and import to Customer 360 using our CSV connector.** To import data to Customer 360, you need to create a data source. It’s recommended to have multiple data sources based on your sources of the data as it allows you to have different refresh schedules and credentials for refresh.

## Bring your data into Customer 360 

***Important Note***: At this point, on-prem data sources are not supported in Customer 360. 
We hope to enable that option soon.

### Step 1 (mandatory): Creating a new data source
To load data to Customer 360 follow the following process:

1. Navigate to **Data Sources** from the **Data Manager page:**

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-tile.png "Get data tile")

2. Click **Get data** as shown below:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-add.png "Get data add")

3. **Provide a name** for the data source and select **Save**. This will create the data source for you. 

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-create.png "Get data create")

### Step 2 (mandatory): Adding Entities
Within the next step you will add **entities** to your data source. In Customer 360 **entities are datasets**. For example, If you have a database that includes multiple datasets about your customers, each of these datasets is an **entity** (an **Orders** dataset, a **Sales** dataset, etc). 

1. In order to start ingesting entities, pick one of the many available connectors that are available in the screen below.
- **Note that some of the following data sources are not supported at this point, including on-prem sources and OData**. 

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-select-source.png "Get data select source")

- **If you wish to load data from Dynamics 365, make sure to choose the  *Common Data Service for Apps* connector shown below:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-connection-settings.png "Get data connection settings")
   
- **Lastly, note that some of the following connectors replaced older connector versions. For example, if you wish to Utilize the Dynamics 365 AX connector, you should choose the *Common Data Service for Apps* option.**

2. After choosing a connector, you will be required to fill some fields. For further guidance around filling those fields for some of the most common data sources (Dynamics 365, csv. and excel files, Blub storage, Azure SQL Database, etc), review the **Common Connectors Definitions** sub-section **that can be found under this section** in the left table of contents.  

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-connection-settings.png "Get data connection settings")

3. At this point you should use the power query window **to select all the entities that you want to load:**

//

**In this step you can also transform the data.** To avoid data-related issues, you should complete the next few transformations:

- If you are ingesting data from a .CSV file and the first row has headers you should select **Transform Table** to do the following:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-transform-table.png "Get data transform table")

- If your data includes **Day Time** columns, you should define those as **Text** type columns by...:

//add image 1

In addition, it is highly recommended to map your data to standard format of data. Customer 360 allows you to map your data to the **Microsoft Common Data Model (CDM)**. In order to do so, select **Map to Standard**, and then map fields from your source data to CDM fields:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-map-entity.png "Map to standard entity")

4. Select **Save** to save the data source:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-map-contact.png "Map to standard entity Contact")

5. After saving, select **Refresh** to load the data to Customer 360:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-map-contact.png "Map to standard entity Contact")

Note: In the future this step will happen automatically.

**At this point, repeat the same steps for each datasource you wish to ingest to Customer 360.**

### Step 3 (optional): Reviewing Ingested Data
Customer 360 will take a couple of minutes to load the data. After successfully refreshing, the ingested data can be reviewed from the **Entities page** as shown below. For more information on the **Entity Page** visit the **Entities section**.

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-entities-data.png "Data manager entities")

### Step 4 (optional) Editing existing data sources
Note: The **Edit** operation is only available for Data sources that are not currently refreshing. 
Follow the below steps to edit an existing data source: 

1. Browse to the data source that you wish to edit:

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-source.png "Get data source")

2. Click on the **Edit** button to edit the data source in Power Query: 

   > [!div class="mx-imgBorder"] 
   > ![](media/data-manager-get-data-source-edit.png "Get data source Edit")

3. Lastly hit **Save** as we did when we originally created our data source

### Next steps: 
At this point you are ready to unlock unique customer insights through the mandatory **Configure Data** sections (those include **Map**,**Match** and **Merge**). If you first wish to review all the entities that were ingested, visit the **Entities** section first. 

