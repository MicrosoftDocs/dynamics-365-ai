---
title: "Export destinations | Microsoft Docs"
description: "The Export destinations page lets you export data and manage destinations for exporting data."
ms.date: 02/05/2020
ms.reviewer: philk
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Export destinations

The **Export destinations** page shows you all locations you've set up to export data to. You can also add new destinations for export. Additionally, it shows extensibility options currently available in Customer Insights. Get a quick overview, description, and find out what you can do with each extensibility option. Export unified profiles, measures, and segments to supported apps relevant for your business.

Go to **Admin** > **Export destinations** to find the following extensibility options:

- [Dynamics 365 Customer Card Add-in](pm-customer-card-addin.md)
- [Power Automate connector](power-automate-connector.md)
- [Power Apps connector](pm-powerapps-connector.md)
- [Power BI connector](pm-connectors.md)
- [Dynamics 365 Sales](#dynamics-365-sales)
- [Dynamics 365 Marketing](#dynamics-365-marketing)
- [Azure Blob Storage](#azure-blob-storage)
- [Connector to LiveRamp&reg;](export-liveramp.md)
- [Customer Insights API](pm-apis.md)

## Add a new Export destination

To add or edit export destinations, you'll need to be an administrator of your Dynamics 365 Customer Insights instance.

### Azure Blob storage

1. On the **Export destinations** page, select **Add destination**.

2. Select **Azure Blob storage** in the **Type** drop-down list.

3. Enter the **Account name**, **Account key**, and **Container** for your Azure Blob storage account.
    - To learn more about how to find the Azure Blob storage account name and account key, see [Manage storage account settings in the Azure portal](https://docs.microsoft.com/azure/storage/common/storage-account-manage).
    - To learn how to create a container, see [Create a container](https://docs.microsoft.com/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

   > [!div class="mx-imgBorder"]
   > ![Add destination](media/export-destinations-azure-blob.png "Add destination")

4. Give your destination a recognizable name in the **Display name** field.

5. Select **Next**.

6. Select the box next to each of the entities you want to export to this destination.

7. Select **Save**.

Your export should start shortly if all prerequisites for export have been completed. The export will also run with every scheduled refresh. To learn more about scheduling, see [Schedule tab](pm-settings.md#schedule-tab).

#### Azure Blob storage locations

Data exported from the Export process will be stored in the Azure Blob storage container you set in your export destination.  The following folder paths are automatically created in your container:

- Customer Insights generated entities: Dynamics365CustomerInsights/Export/%EntityName%/%EntityName%_%PartitionId%.csv
  - Example: Dynamics365CustomerInsights/Export/Customer/Customer_1.csv
- Data Source entities: Dynamics365CustomerInsights/Export/%DataSourceName%_%EntityName%/%DataSourceName%_%EntityName%_%PartitionId%.csv
  - Example: Dynamics365CustomerInsights/Export/Retail_Contacts/Retail_Contacts_1.csv

### Dynamics 365 Sales

1. On the **Export destinations** page, select **Add destination**.

2. Choose **Dynamics 365 Sales** in the **Type** drop-down list.

3. Define your Dynamics 365 Sales URL in **Server address**, select **Sign in**, and select a Dynamics 365 Sales account.

   > [!div class="mx-imgBorder"]
   > ![Add destination page](media/export-destinations-dynamics365-for-sales.png "Add destination page")

4. Give your destination a recognizable name in **Display name**.

5. Select **Add**.

### Dynamics 365 Marketing

1. On the **Export destinations** page, select **Add destination**.

2. Choose **Dynamics 365 Marketing** in the **Type** drop-down list.

3. Define your Dynamics 365 Marketing URL in **Server address**, select **Sign in**, and select a Dynamics 365 Marketing account.

4. Give your destination a recognizable name in **Display name**.

5. Select **Add**.

## View Export destinations

If you've already created any destinations, you'll see them listed in a table on the **Export destinations** page. This table has three columns:

- **Display name**: The name you entered when creating the destination.
- **Type**: The destination type you set when creating the destination.
- **Created**: The date you created the destination.

## Remove an Export destination

To remove an Export destination, start from the main **Export destinations** page.

1. Select the vertical ellipsis for the Export destination you want to remove.

   > [!div class="mx-imgBorder"]
   > ![Vertical ellipsis](media/export-destinations-page-ellipsis.png "Vertical ellipsis")

2. Select **Remove** from the dropdown menu.

3. Confirm the removal by selecting **Remove** on the confirmation screen.
