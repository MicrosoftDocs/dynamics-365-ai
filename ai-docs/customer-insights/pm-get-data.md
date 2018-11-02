---
title: "Get data | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/1/2018
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
# Get Data

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Get data in Customer 360 help you bring data into your Customer 360 instance. This is a pre-requisite to start configuring Customer 360. You can bring data to Customer 360 by using the 20+ out of the box connectors that we make available for sources like Dynamics 365, SQL Azure, Blob store etc. Even if you don’t find an out of the box connector for your source, you can always export the data from your source as a CSV file and import to Customer 360 using our CSV connector. To import data to Customer 360 you need to create a data source. Its recommended to have multiple data sources based on the source of the data as it allows for having different refresh schedules, credentials for refresh etc. 

### Step 1 (mandatory): Creating new data source
To load data to Customer 360 follow the below process:

- **1.Navigate to Get data from the Data Manager page:**

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-tile.png "Get data tile")

- **2.Click **Add Data** as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-add.png "Get data add")

- 3.**Provide a name and description** for the data source and **hit “Create”.** This will create the data source for you. 

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-create.png "Get data create")

### Step 2 (mandatory): Adding Entities
Next step is to add **Enntities** to the data source. In Customer 360 **Entities are datasets**. For example, If you have a database that includes multiple datasets about your customers, each of these data sets is considered to be an **Entity** (for example an **Orders** dataset, a **Sales** data set, etc). 

- 1.In order to start ingesting entities, pick one of the many available data sources and provide the connection string and connection credentials. Lastly, hit **Next**:

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-select-source.png "Get data select source")


> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-connection-settings.png "Get data connection settings")

- 2.From the list of available entities, select the entity that you want to load. **In this step you can also perform transformation on the data.** For example, if you are ingesting data from CSV file and the first row has headers then you can use the **Transform Table** tab to select that transformation as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-transform-table.png "Get data transform table")

One other highly recommended transform is “Map to standard”. Customer 360 allows you to map data to Microsoft Common data model (CDM) during your ingestion process. In order to do this, click in the transform “Map to standard” and from the option map fields from your source data to CDM fields as show below: 

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-map-entity.png "Map to standard entity")

- 3.Now click **Create** and this gives you the option to “Save” the data source:

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-map-contact.png "Map to standard entity Contact")

- 4.After you “Save” the data source, hit **Refresh** to load data to Customer 360. 

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-map-contact.png "Map to standard entity Contact")

Note: In the future this step will happen automatically. 

### Step 3 (optional): Reviewing the Ingested Data
Customer 360 will take a couple of minutes to load the data. After a successful refresh, the ingested data can be reviewed from the Entities tab as shown below. For more information on the **Entity Page** visit the **Entities section**

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-map-custom.png "Map to standard entity Custom")

**Repeat the same set of steps for as many data sources that you want to ingest data into Customer 360.**

### Step 4 (optional) Editing existing data sources
Edit operation is only available for Data sources that is not currently refreshing. Follow the below steps to edit an existing data source: 

- 1.Browse to the data source to be edited:

> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-source.png "Get data source")

- 2.Click on the **Edit** button to edit the data source in Power query. 


> [!div class="mx-imgBorder"] 
> ![](media/data-manager-get-data-source-edit.png "Get data source Edit")


### Next step: 
Now you are ready to unlock unique customer insights through the **Data Configure** sections (those include **Map**, **Match** and **Merge**). If you wish to review all the entities that were ingested as part of the **Get Data** process, review the **Entities** section first. 
