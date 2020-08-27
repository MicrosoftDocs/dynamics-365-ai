---
title: "Home page in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Start exploring the app on the Home page in Dynamics 365 Customer Insights."
ms.date: 08/27/2020
ms.reviewer: nimagen
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Start your journey in Customer Insights on the Home page

You can [access your Customer Insights instance](https://home.ci.ai.dynamics.com/) on the following URL: [https://home.ci.ai.dynamics.com/](https://home.ci.ai.dynamics.com/).
The first page you'll see in Dynamics 365 Customer Insights is **Home**. This page shows an overview of your customer base and key metrics to track the health of your business.

> [!div class="mx-imgBorder"] 
> ![Insights on Home page](media/home-page-insights.png "Insights on Home page")

## Explore the home page

Under **Recent segments**, you see groups of customers based on demographic, behavioral, or transactional attributes that you've defined. [Creating segments](segments.md) helps you to better target your business activities.

**Recent measures** shows tiles with [measures](measures.md). Measures are key performance indicators (KPIs) that you've defined. For example, average likelihood of customer churn or average online spend per customer.

The **Recent enrichments** section lists the results of the enrichment runs that completed recently. Enrichments add information about your customer base. For example, by understanding the interests and brands that they have affinity for. This information can be unlocked using the [enrichment](enrichment-microsoft-graph.md) capabilities, after completing the [map](map-entities.md), [match](match-entities.md), and [merge](merge-entities.md) phases.

## Change between environments

Once you've set up and configured [data sources](data-sources.md), you'll want to switch from a demo environment to a live environment. Using the production environment lets you work with your own customer data. Select the **Environment** control in the upper-right corner of the page to change environments.

> [!div class="mx-imgBorder"] 
> ![Switch environment](media/home-page-environment-switcher.png "Switch environment")

Administrators can create and manage [multiple environments](manage-environments.md). Maintaining more than one environment may be useful if, for example, your organization operates internationally and you need to segregate data and insights in different ways.

## Next step

To see your own insights on the home page, you'll first need to [add data sources](data-sources.md) and [unify](data-unification.md) your data to build customer profiles.
