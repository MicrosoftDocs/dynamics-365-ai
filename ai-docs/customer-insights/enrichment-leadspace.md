---
title: "Enrichment of company profiles with the third party enrichment Leadspace in Dynamics 365 Customer Insights | Microsoft Docs"
description: "General information about the Leadspace third party enrichment in Customer Insights."
ms.date: 05/06/2020
ms.reviewer: mhart
ms.service: dynamics-365-ai
ms.topic: "article"
author: adasatu
ms.author: a-dasatu
manager: shellyha
---

# Enrichment of company profiles with Leadspace (preview)

Leadspace is a data science company that provides a B2B Customer Data Platform. As a third party data provider, Leadspace enables customers who have unified customer profiles for companies to enrich them with attributes including company size, location, industry and more.

## Prerequisites

To configure Leadspace, the following prerequisites must be met:

- You have active Leadspace license and the “perpetual key” (referred to as **Leadspace token** in Customer Insights). Please reach out directly to [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) for details about their product.
- You have the [Administrator](pm-permissions.md#administrator) role in Customer Insights.
- You have [unified customer profiles](pm-profiles.md) for companies.

## Configuration

1. Go to **Data** > **Enrichment**.

1. Select **Set up** on the Leadspace tile.

1. Select **Add token** and enter an active **Leadspace token** (perpetual key). Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox. Confirm both inputs by selecting **Apply**.

   > [!div class="mx-imgBorder"]
   > ![Leadspace configuration page](media/enrichment-leadspace-configuration.png "Leadspace configuration page")

1. Select **Add data** and define which fields from your unified profiles should be used to look for matching company data from Leadspace. The **company name** field is required. For a higher match accuracy, up two other fields, **company website** and **company location**, can be added.

1. Select **Save** to complete the field mapping.

1. Select **Run** to enrich the company profiles. How long an enrichment run takes depends on the number of unified customer profiles. Expect it to take at least 1 minute per 1.000 profiles.

## Enrichment results

After running the enrichment you can review the newly enriched company data under [My enrichments](pm-profiles.md). You can find the time of the last update and the number of enriched profiles.

You can access a detailed view of each enriched profile by selecting **View enriched data**.

For more information, see [Leadspace APIs](https://support.leadspace.com/hc/en-us/sections/201997649-API).
