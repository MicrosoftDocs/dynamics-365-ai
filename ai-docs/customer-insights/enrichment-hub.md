---
title: "Enrich customer profiles in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Use capabilities to enrich your customer data in Dynamics 365 Customer Insights."
ms.date: 08/03/2020
ms.reviewer: kishorem
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Enrichment for customer profiles (preview)

Use data from sources like Microsoft and other partners to enrich your customer data.

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Enrichment hub page in Customer Insights":::

In Customer Insights, go to **Data** > **Enrichment** to work with enrichment options.    
You need to have Contributor or Administrator permissions to create or edit enrichments. For more information, see [Permissions](permissions.md).

On the **Discover** tab, you'll find the following enrichments:

- [Brands](enrichment-microsoft-graph.md) provided by Microsoft Graph
- [Interests](enrichment-microsoft-graph.md) provided by Microsoft Graph
- [Company data provided by Leadspace](enrichment-leadspace.md)

On the **My enrichments** tab, you can see the enrichments you've configured and edit their properties.

## Manage existing enrichments

Go to the **My enrichments** to see all configured enrichments. Each enrichment is represented as a row that includes additional information about the enrichment.

Select an enrichment to see the available options. Alternatively, you can select the ellipsis (...) on a list item to see the options.

:::image type="content" source="media/enrichment-hub-options.png" alt-text="Options to manage enrichments in the list of enrichments":::

- **View** enrichment details with the number of enriched customer profiles.
- **Edit** the enrichment configuration.
- **Refresh** the enrichment to update customer profiles with the latest data.
- **Deactivate** an existing enrichment to stop it from refreshing automatically with every scheduled refresh. Data from the last successful refresh will continue to be available.
- **Activate** an inactive enrichment to restart automatic refreshing with every scheduled refresh.

You can refresh or deactivate multiple enrichments at once by selecting them in the list. View and edit options aren't available as bulk action and only work for one enrichment at a time.
