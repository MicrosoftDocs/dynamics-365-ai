---
title: "Common Connectors Guidance | MicrosoftDocs"
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
# Common Connectors Guidance

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Common Connectors Guidance

***Important Note***: At this point (Novemebr 2018), on-prem data sources are not supported in Customer 360. 
We hope to enable that option soon.

### Ingest data from an Excel file (text/csv.)

1. If it’s a desktop file, you should first save it in SharePoint (as explained here: [https://support.office.com/en-us/article/Work-with-worksheet-data-in-OneDrive-C051A205-1C06-4FEB-94D8-793B0126B53A](https://support.office.com/en-us/article/Work-with-worksheet-data-in-OneDrive-C051A205-1C06-4FEB-94D8-793B0126B53A).

2. Select the **Text/csv** connector:

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-excel.png "Select Excel")




//Jim can you add the content here? Thanks!




### Ingest data from a file hosted in Azure blob

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-storage.png "Select Azure Blobs")

To ingest data to Dynamics 360 from a csv file hosted in a blob in an Azure subscription, follow these steps.

1. Select Blob connector from the list of connectors.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs.png "Select Azure Blobs")

2. Enter the account name and account key, and then select **Next**.

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
   
### Ingest data from Dynamics 365 for Customer Engagement

Select **Common Data Service for Apps**.

> [!div class="mx-imgBorder"] 
> ![](media/connector-cds.png "Select Common Data Service")

### Ingest data from Azure SQL database

Select **SQL Server database**.

> [!div class="mx-imgBorder"] 
> ![](media/connector-sql-database.png "Select SQL database")
