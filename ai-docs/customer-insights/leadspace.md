---
title: "Enrichment of company profiles with the third party enrichment Leadspace in Dynamics 365 Customer Insights | Microsoft Docs"
description: "General information about the Leadspace third party enrichment in Customer Insights."
ms.date: 04/27/2020
ms.reviewer: mhart
ms.service: dynamics-365-ai
ms.topic: "article"
author: adasatu
ms.author: a-dasatu
manager: shellyha
---

# Enrichment of company profiles with Leadspace (preview)

Leadspace is a software as a service (SaaS) Data Science Company. As a 3rd party data provider, Leadspace will allow customers who have B2B profiles to enrich them with attributes including company size, location, industry and more.

## Prerequisites

To configure Leadspace, the following prerequisites must be met:
-	An active Leadspace license, the “perpetual key” (referred to as “Leadspace token” in Customer Insights). Please reach out directly to [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) for details about their product.
-	You have the [Administrator](pm-permissions#administrator) role in Customer Insights.
-	You have [unified customer profiles](pm-profiles).

## Configuration

1. Enter an active Leadspace token (perpetual key) and tick the checkbox if you agree to the stated privacy policy.

   > [!div class="mx-imgBorder"]
   > ![Leadspace configuration page](media/enrichment-leadspace-configuration.png "Entity name format")

2.	Define which fields from your unified profiles should be used to lookup for matching company data from Leadspace. The **company name** field is required, but in order to allow for a better match up two other fields, **company website** and **company location**, can be added.
**Save** to complete the field mapping.

3.	Click the **run** button. The execution time of an enrichment run depends on the number of unified customer profiles. On average expect it to take at least 1 minute per 1.000 profiles. 

## Enrichment results

After running the enrichment you can review the newly enriched company data under [My enrichments](pm-profiles). You can find out when your last update took place and the amount of enriched profiles.
You also have the possibility to access a detailed view of each enriched profile by clicking on the “View enriched data” button.
[Learn more about the Leadspace APIs](https://support.leadspace.com/hc/en-us/sections/201997649-API).
