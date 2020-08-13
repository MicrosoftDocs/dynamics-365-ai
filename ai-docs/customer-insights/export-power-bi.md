---
title: "Power BI connector | Microsoft Docs"
description: "Learn how to use the Dynamics 365 Customer Insights connector in Power BI."
ms.date: 04/14/2020
ms.reviewer: sthe
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Connector for Power BI (preview)

Create visualizations for your Customer Insights data with the Power BI Desktop Add-in. Generate additional insights and build reports with your unified customer data.

## Prerequisites

- You have unified customer profiles in Customer Insights.
- The latest version of [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) is installed on your computer. [Learn more about Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-what-is-desktop).

## Configure the connector for Power BI

1. In Power BI Desktop, select **File** > **Get Data**.

1. Select **See more** and search for **Dynamics 365 Customer Insights**

1. Select the result and select **Connect**.

1. **Sign in** with the same organizational account you use for Customer Insights and select **Connect**.

1. In the Navigator dialog box. you see the list of all Customer Insights instances you have access to. Expand an instance and open any of the folders (Entities, Measures, Segments, Enrichments). Open e.g. the **Entities** folder, to see all entities you can import.

   ![Power BI Connector Navigator](media/power-bi-navigator.png "Power BI Connector Navigator")

1. Select the check boxes next to the entities to include and **Load**. You can select multiple entities from multiple environments.

1. You'll see a loading dialog box while your entities are loaded. Once all of your selected entities have loaded, you can use the capabilities of Power BI on Customer Insights data.

## Large data sets
The Customer Insights connector for Power BI is designed to work for data sets up to 1 Million CI profiles. Importing larger data sets may work, but needs a long time and there is a risk of a time out due to limitatons on Power BI's side. [Learn more about Power BI's recommendation for large data sets](https://docs.microsoft.com/en-us/power-bi/admin/service-premium-what-is#large-datasets). 

### Workaround
* Consider working with a subset of your Customer Insights data, by creating [Segments](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/segments) instead of exporting all Customer Insights entities to Power BI.
