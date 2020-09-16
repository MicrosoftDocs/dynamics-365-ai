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

Adding data sources based on Power Query connectors usually follow the same steps as outlined below. For details about specific connectors, refer to the linked articles in the Power Query connector reference.

## Add a data source through Power Query connectors

As an example, we'll connect to a CSV file with customer data hosted on an Azure Blog storage account.

1. In Customer Insights, create a new data source.

2. Select **Azure Blob storage** from the list of connectors.

3. Enter the **Account name** and **Account key**, then select **Next**.

   > [!NOTE]
   > You can find your account name and key from the **Access keys** area in the Azure admin portal.

4. You now see a folder structure with all containers in the Blob storage. Select the container that includes your CSV file, and select **Next**.

5. You now see the available CSV files in the container. Select **[Table]** in the content column to see a preview of the file's content.

   > [!div class="mx-imgBorder"]
   > ![Select Table control in CSV file](media/connector-azure-blobs-preview.png)

## Transform Power Query entities

Link to PQ content for transforming entities. Aditya to review closely if we cover customer use cases properly.

## Available Power Query data sources

This article covers the list of available data sources to ingest data into Dynamics 365 Customer Insights. For more information about adding a data source in the app, see [Connect data sources](data-sources.md).

The **Choose data source** page organizes data types in the following categories:

- [File](#file-data-sources)
- [Database](#database-data-sources)
- [Power Platform](#power-platform-data-sources)
- [Azure](#azure-data-sources)
- [Online services](#online-services-data-sources)
- [Other](#other-data-sources)

### File data sources

The File category provides the following data connections:

- Access
- Excel
- Folder
- JSON
- PDF
- SharePoint folder
- Text/CSV
- XML

### Database data sources

The Database category provides the following data connections:

- Amazon Redshift
- Google BigQuery
- IBM Db2 database
- Impala
- MySQL database
- Oracle database
- PostgreSQL database
- SQL Server database
- Sybase database
- Teradata database
- Vertica

### Power Platform data sources

The Power Platform category provides the following data connections:

- Common Data Service

### Azure data sources

The Azure category provides the following data connections:

- Azure Blobs
- Azure Data Lake Storage Gen2
- Azure HDInsight Spark
- Azure SQL Data Warehouse
- Azure SQL database
- Azure Tables

### Online services data sources

The Online services category provides the following data connections:

- Microsoft Exchange Online
- Salesforce objects
- Salesforce reports
- SharePoint Online list

### Other data sources

The Other category provides the following data connections:

- Active Directory
- OData
- Odbc
- SharePoint list
- Spark
- Web API
- Web page
- Blank table
- Blank query



