---
title: "Data sources in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Learn how to import data from various sources into Dynamics 365 Customer Insights."
ms.date: 09/29/2020
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
ms.assetid: 
author: m-hartmann
ms.author: mhart
ms.reviewer: mukeshpo
manager: shellyha
---

# Overview about data sources

Customer Insights connects data from a broad set of sources. Connecting a data source to Customer Insights is often referred to as the process of *data ingestion*. After bringing th data into customer Insights, you can [unify](data-unification.md) the data and get a holistic view of the customer data, and take action on it.

## Add a data source

Please refer to the detailed articles on how to add a data source, depending on which option you choose.

You can add a data source in three main ways:

- [Through dozens of Power Query connectors](connect-power-query.md)
- [From a Common Data Model folder](connect-common-data-model.md)
- [From your own Common Data Service lake](connect-common-data-service-lake.md)

> [!NOTE]
> You can't add data from on-premises data sources yet.

## Review ingested data

You'll see the name of each ingested data source, as well as its status and the last time the data was refreshed for that source.

> [!div class="mx-imgBorder"]
> ![Data source added](media/configure-data-datasource-added.png "Data source added")

|Status  |Description  |
|---------|---------|
|Available   |Data source was successfully ingested if a date and time are shown. Or, data source doesn't need to be ingested, if no date and time are shown.          |
|Needs entities   |The data source has no data ingested yet.         |
|Refreshing    |Data ingestion is in progress. You can cancel this operation by selecting **Stop refreshing** in the **Actions** column. Stopping the refresh of a data source will revert it to its last refresh state.       |
|Unable to refresh     |Data ingestion ran into errors. Select the **See details** link to review the errors within 24 hours of the time of failure.         |

Loading data can take some time. After a successful refresh, the ingested data can be reviewed from the **Entities** page. For more information, see [Entities](entities.md).

## Delete a data source

1. In Customer Insights, go to **Data sources**.

2. Select the vertical ellipsis next to the data source you want to remove and select **Delete** from the drop-down menu.

3. Confirm your deletion.