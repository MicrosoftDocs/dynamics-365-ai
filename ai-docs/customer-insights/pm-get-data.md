---
title: "Get data | MicrosoftDocs"
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
# Get Data

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

**You can bring in data to Customer 360 by using the 20+ out-of-the-box connectors** that we make available for sources, such as Dynamics 365, SQL Azure, and Blob store. Even if you don’t find a suitable out-of-the-box connector for your source, **you can always export the data from your source as a CSV file and import to Customer 360 using our CSV connector.** To import data to Customer 360, you need to create a data source. It’s recommended to have multiple data sources based on your sources of the data as it allows you to have different refresh schedules and credentials for refresh.

## Common Connectors Guidance

### Ingest data from Dynamics 365 for Customer Engagement

Select **Common Data Service for Apps**.

> [!div class="mx-imgBorder"] 
> ![](media/connector-cds.png "Select Common Data Service")

### Ingest data from Azure SQL database

Select **SQL Server database**.

> [!div class="mx-imgBorder"] 
> ![](media/connector-sql-database.png "Select SQL database")

### Ingest data from Excel

1. If it’s a desktop file (text/csv), you should first either upload it to OneDrive or save it in SharePoint (as explained here: [https://support.office.com/en-us/article/Work-with-worksheet-data-in-OneDrive-C051A205-1C06-4FEB-94D8-793B0126B53A](https://support.office.com/en-us/article/Work-with-worksheet-data-in-OneDrive-C051A205-1C06-4FEB-94D8-793B0126B53A).

2. Select **Excel**.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-excel.png "Select Excel")

3. Provide the URL to your online file location.

### Ingest data from a csv file

1. Upload the file to a blob storage account (create an account if needed).

2. Select **Azure Blobs**.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs.png "Select Azure Blobs")

3. Continue through steps 2-4 for Blob below.

### Ingest data from a file hosted in Azure blob

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-storage.png"Select Azure Blobs")

To ingest data to Dynamics 360 from a csv file hosted in a blob in an Azure subscription, follow these steps.

1. Select Blob connector from the list of connectors.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs.png "Select Azure Blobs")

2. Enter the account name and account key, and then select ***Next**.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-account-name-key.png "Enter Blob account name and key")

   **Note**: You can find the account name and key from **Access keys** in the Azure portal as show below: 

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-access-keys.png "Blob access keys")

3. This will now list out all the containers in the blob, select the container with the CSV file and click next. 

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-container.png "Get data tile")

4.	Now you will see the various csv files in the container, click on **[Table]** in the content column to expand and see the file content preview. 

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-preview.png "Get data tile")

## Get data steps

### Step 1 (mandatory): Creating a new data source
To load data to Customer 360 follow the following process:

1. Navigate to **Get Data** from the **Data Manager page:**

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-tile.png "Get data tile")

2. Click **Add Data** as shown below:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-add.png "Get data add")

3. **Provide a name and description** for the data source and select **Create**. This will create the data source for you. 

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-create.png "Get data create")

### Step 2 (mandatory): Adding Entities
Within the next step you will add **entities** to your data source. In Customer 360 **entities are datasets**. For example, If you have a database that includes multiple datasets about your customers, each of these data sets is an **entity** (such as an **Orders** dataset, a **Sales** dataset, etc). 

1. In order to start ingesting entities, pick one of the many available data sources that are available within the screen below:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-select-source.png "Get data select source")
  
2. After choosing a data source, you will be required to fill some fields as shown in the example below. For further guidance around filling those fields for some of the most common data sources (Dynamics 365, csv. and excel files, Blub storage, Azure SQL Database, etc), review the **Common Connectors Definitions** sub-section **that can be found under this section** in the left menu. 

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-connection-settings.png "Get data connection settings")

3. From the list of available entities, select the entity that you want to load. **In this step you can also transform the data.** For example, if you are ingesting data from a .CSV file and the first row has headers then you can select **Transform Table** to do the following:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-transform-table.png "Get data transform table")

In addition, it is highly recommended to map your data to standard format of data. Customer 360 allows you to map your data to the **Microsoft Common Data Model (CDM)** during your ingestion process. In order to do so, select **Map to Standard**, and then map fields from your source data to CDM fields:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-map-entity.png "Map to standard entity")

4. Select **Save** to save the data source:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-map-contact.png "Map to standard entity Contact")

5. After saving, select **Refresh** to load the data to Customer 360:

  > [!div class="mx-imgBorder"] 
  > ![](media/data-manager-get-data-map-contact.png "Map to standard entity Contact")

Note: In the future this step will happen automatically.

**At this point, repeat the same steps for each data source into which you want to ingest data using Customer 360.**

### Step 3 (optional): Reviewing the Ingested Data
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
At this point you are ready to unlock unique customer insights through the **Data Configure** sections (those include **Map**, **Match** and **Merge**). If you wish to review all the entities that were ingested as part of the **Get Data** process, review the **Entities** section first. 

// To add to a seperate sub-section that will be called *Common Connectors Definitions*:

// To add to a seperate sub-section that will be called *Recommended Trasformations*:
