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

# Start your journey in Customer Insights 

You can [access your Customer Insights instance](https://home.ci.ai.dynamics.com/) on the following URL: [https://home.ci.ai.dynamics.com/](https://home.ci.ai.dynamics.com/).

## Creating your first Trial environment
Upon providing your AAD credentials and work email the first screen you will see is used for the creation of your first environment.

Follow those steps:
1.	Name your environment
2.	Select Trial type
3.	Select your Region 
4.	(Optional and available only for Dynamics 365 admins): If you wish to use the predictive capabilities of Customer Insights (Customer churn, etc), click Advanced settings and then enter the server URL of your organization.
5.	Click Create 

Upon successful instance creation, the next screen you will see it the **demo instance** one.

This instance allows you to experiment with Customer Insights while utilizing non-real demo data. 

**Note:** You can also tweak the demo instance data to match your specific industry by clicking the **Settings icon** at the top menu and then hitting **Demo settings**. You can also change the theme for your trial instance using any of the themes in this panel. 

Once you are ready to use your real environment, click the **Environment button** at the top bar menu and then choose the environment you have just created from the panel in order to switch to it. Note that your trial instance will expire after 30 days. After that timeline you will be prompted to either buy or delete this instance.

## Creating your first Production or Sandbox environment
In your trial environment, click the **Settings icon** at the top menu and then hit **New environment.** 

Follow the steps mentioned above for setting up a new Trial instance. The only difference from the experience mentioned above for Trial is that you will be able to save your data to another location besides Customer Insights storage. You can save it to *Azure Data Lake Storage (ADLS)*. 

To achieve that, click **Advanced settings** and then provide your account name and account key. 

**Important:** By saving data to Azure Data Lake Storage, you agree that data will be transferred to and stored in the appropriate geographic location for that Azure storage account, which may differ from where data is stored in Dynamics 365 Customer Insights. Learn more by visiting the *Microsoft Trust Center.* 

## Explore the home page
The **Home page** shows an overview of your customer base and key metrics to track the health of your business.

> [!div class="mx-imgBorder"] 
> ![Insights on Home page](media/home-page-insights.png "Insights on Home page")

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
