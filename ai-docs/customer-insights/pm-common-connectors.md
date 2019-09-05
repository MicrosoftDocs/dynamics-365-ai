---
title: "Common connectors guidance | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 04/01/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
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
# Common connectors

This section provides more information atop the **Data Sources** section. 
In this section we will cover in detail how to load data from several connectors. Currently this
section covers the following connectors (in that order):
1. Ingest data from a file hosted in an **Azure blob**
2. Ingest data from **Dynamics 365**
3. Ingest data from the **Azure SQL database**
4. Ingest data from a **CSV file** 

> [!IMPORTANT]
> Currently, on-premises and OData data sources are not supported in Dynamics 365 Customer Insights. 

## Ingest data from a file hosted in an Azure blob

> [!div class="mx-imgBorder"] 
> ![Select Azure blobs](media/connector-azure-storage.png "Select Azure blobs")


<!-editor note: The alt/hover text above is the same as for the image below. Is that correct? -->


To ingest data to Customer Insights from a CSV file hosted within a blob location in a Microsoft Azure subscription, follow these steps:

1. Select **Azure Blobs** from the list of connectors.

   > [!div class="mx-imgBorder"] 
   > ![Select Azure Blobs](media/connector-azure-blobs.png "Select Azure Blobs")

2. Enter the account name and account key, and then select **Next**.

   > [!div class="mx-imgBorder"] 
   > ![Enter blob account name and key](media/connector-azure-blobs-account-name-key.png "Enter blob account name and key")

   > [!NOTE]
   > You can find the account name and key from the **Access keys** part of the Azure portal as shown in the following example. 

    > [!div class="mx-imgBorder"] 
    > ![Blob access keys](media/connector-azure-blobs-access-keys.png "Blob access keys")

3. You will now see a list of all the containers in the blob. Select the container that includes your CSV file, and select **Next**.

   > [!div class="mx-imgBorder"] 
   > ![Get data tile](media/connector-azure-blobs-container.png "Get data tile")

4.	You will see the various CSV files in the container. Select **[Table]** in the content column to see a preview of the file's content.


<!--editor note: alt/hover text above is same as for image below. Is that right? -->


    > [!div class="mx-imgBorder"] 
    > ![](media/connector-azure-blobs-preview.png "Get data tile")
   
## Ingest data from Dynamics 365

1. Select **Common Data Service**.

   > [!div class="mx-imgBorder"] 
   > ![Select Common Data Service](media/connector-cds.png "Select Common Data Service")
 
2. Enter your server URL.

   > [!div class="mx-imgBorder"] 
   > ![Provide server URL](media/connector-provide-server-url.png "Provide server URL")

3. Sign in with your username and password.

4. Choose your entities of interest from the left-side menu, and then review them on the right-side window:


<!--editor note: Is "Log in" accurate alt/hover text for the next image? I don't see any sign-in area. -->

   > [!div class="mx-imgBorder"] 
   > ![Log in](media/connector-ce-log-in.png "Log in")

   > [!div class="mx-imgBorder"] 
   > ![Connector account](media/connector-account.png "Connector account")

## Ingest data from the Azure SQL database

1. Select **SQL Server database** from the connector list.

   > [!div class="mx-imgBorder"] 
   > ![Select SQL Server database](media/connector-select-sql-server-database.png "Select SQL Server database")

3. Enter your database server, database name, username, and password.

   > [!div class="mx-imgBorder"] 
   > ![Provide database settings](media/connector-provide-database-settings.png "Provide database settings")

4. Choose data from the specific tables you want to bring into Customer Insights.

   > [!div class="mx-imgBorder"] 
   > ![Pick data from tables](media/connector-pick-data-from-tables.png "Pick data from tables")
   
## Ingest data from a CSV file

1. If the CSV file that contains the data you want to ingest is a desktop file, you should first save it in SharePoint as explained here: [Work with worksheet data in OneDrive](https://support.office.com/article/Work-with-worksheet-data-in-OneDrive-C051A205-1C06-4FEB-94D8-793B0126B53A)

2. Select the **Text/CSV** connector.

   > [!div class="mx-imgBorder"] 
   > ![Select Excel](media/connector-excel.png "Select Excel")

3. Manually format the URL to your online document.

   Once you copy the URL to your online document from SharePoint, it should look like this: 

   https://microsoft.sharepoint.com/:u:/t/TeamName/EdP4Jh3iCj9DUteIBCzbdOX7C4bmVvzlDo81F0A?e=2Co1vj
   
   Format the URL as follows:

   > [!div class="mx-imgBorder"] 
   > ![Format URL](media/connector-format-url1.png "Format URL")

   The final result for the preceding example is: 

   > [!div class="mx-imgBorder"] 
   > ![Final result](media/connector-format-final-result.png "Final result")

   Here is an example of a copied link: 
 https://microsoft.sharepoint.com/:u:/t/yourTeamName/EdP4G8Jk2dZJh3iCj9DUteIBCzbdOX7C4bmVvzlDo811vj  

From the link components described above:

- Here is where you can find **Your team name**:

  > [!div class="mx-imgBorder"] 
  > ![Team name](media/connector-team-name.png "Team name")

- Here is where you can find the **Root folder to your documents**:

  > [!div class="mx-imgBorder"] 
  > ![Root folder](media/connector-root-folder.png "Root folder")

- And here is where you will find your **File name and the folder structure for the file**:

  > [!div class="mx-imgBorder"] 
  > ![File name and folder structure](media/connector-folder-structure.png "File name and folder structure")
