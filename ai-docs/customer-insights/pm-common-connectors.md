---
title: "Common connectors guidance | MicrosoftDocs"
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
# Common connectors guidance

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> Currently, on-premises and OData data sources are not supported in Customer Insights. 

## Ingest data from an Excel file (text/CSV)

1. If it’s a desktop file, you should first save it in SharePoint (as explained here: [Work with worksheet data in OneDrive](https://support.office.com/article/Work-with-worksheet-data-in-OneDrive-C051A205-1C06-4FEB-94D8-793B0126B53A).

2. Select the **Text/csv** connector:

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-excel.png "Select Excel")

3. Manually formatting the URL to your online document

   Once you copy the URL to your online document from SharePoint, it should look like this: 

   https://microsoft.sharepoint.com/:u:/t/TeamName/EdP4Jh3iCj9DUteIBCzbdOX7C4bmVvzlDo81F0A?e=2Co1vj
   
   And needs to be formatted following these steps:

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-format-url1.png "Format URL")

   The final result for the above will be: 

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-format-final-result.png "Format URL")

 Let's take an example of a copied link: 
 https://microsoft.sharepoint.com/:u:/t/yourTeamName/EdP4G8Jk2dZJh3iCj9DUteIBCzbdOX7C4bmVvzlDo811vj  

**Your team name**

> [!div class="mx-imgBorder"] 
> ![](media/connector-team-name.png "Team name")

**Root folder to your documents**

> [!div class="mx-imgBorder"] 
> ![](media/connector-root-folder.png "Root folder")

**File name and the folder structure for the file**

> [!div class="mx-imgBorder"] 
> ![](media/connector-folder-structure.png "File name and folder structure")

## Ingest data from a file hosted in Azure blob

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-storage.png "Select Azure Blobs")

To ingest data to Dynamics 360 from a CSV file hosted within a blob location in an Azure subscription, follow these steps.

1. Select **Blob connector** from the list of connectors.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs.png "Select Azure Blobs")

2. Enter the account name and account key, and then select **Next**.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-account-name-key.png "Enter Blob account name and key")

   **Note**: You can find the account name and key from the **Access keys** part in the Azure portal as shown below. 

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-access-keys.png "Blob access keys")

3. This will now list all the containers in the blob. Select the container that includes your CSV file and select **Next**.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-azure-blobs-container.png "Get data tile")

4.	Now you will see the various CSV files in the container. Select **[Table]** in the content column to expand and see the file content preview.

    > [!div class="mx-imgBorder"] 
    > ![](media/connector-azure-blobs-preview.png "Get data tile")
   
## Ingest data from Dynamics 365 for Customer Engagement

Select **Common Data Service for Apps**.

> [!div class="mx-imgBorder"] 
> ![](media/connector-cds.png "Select Common Data Service")

Provide your server URL.

> [!div class="mx-imgBorder"] 
> ![](media/connector-provide-server-url.png "Provide server URL")

Log in with your username and password.

> [!div class="mx-imgBorder"] 
> ![](media/connector-ce-log-in.png "Log in")

> [!div class="mx-imgBorder"] 
> ![](media/connector-account.png "Connector account")

## Ingest data from Azure SQL database

Select **SQL Server database** from the connector list.

> [!div class="mx-imgBorder"] 
> ![](media/connector-select-sql-server-database.png "Select SQL Server database")

Select **SQL Server database**.

Provide your database server, database name, username and password.

> [!div class="mx-imgBorder"] 
> ![](media/connector-provide-database-settings.png "Provide database settings")

Pick data from the specific tables you want to bring into Customer Insights.

> [!div class="mx-imgBorder"] 
> ![](media/connector-pick-data-from-tables.png "Pick data from tables")
