---
title: "Enrichment | Microsoft Docs"
description: 
ms.date: 11/25/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Enrichment

Dynamics 365 Customer Insights consolidates customer data from all of your data sources after completing the map, match, and merge phases. At the same time, Customer Insights goes beyond that and provides information about your customers that comes from proprietary data. The **Enrichment** page enables your to get insights from data on affinities for hundreds of brands and dozens of interest-categories. These affinities are extracted from profiles that might be similar to the profile of you customers.

In Customer Insights, go **Enrichment** to configure and view the data.

## Explore the Enrichment page

The **Enrichment** page includes two major sections where you define the parameters to enrich your data.

![Screenshot of the Enrichment page in Customer Insights](media/configure-data-enrich-profile-page.png)

- **Demographics**: Define demographics for a specific group of profile types for which you want to gain insights around preferred brands and interests.

- **Brands and categories**: Select wether Customer Insights delivers the insights about groups of profiles based on your own selections or based on selecting an industry.

## Demographics section

You need to define the values for at least two fields to enrich your unified customer profiles.

The following formats and values are supported:

- **Date of Birth**: m/d/yyyy, mmmm d, yyyy-mm-dd, mmmm yyyy
- **Gender**: Male, Female, Unknown
- **Zip Code**: 5-digit US ZIP Code (only supported for the US)

## Brands and categories section

Choose one of the following options. Then, provide the information for that option.

- **Choose on my own**: This option allows you to choose brands and interest-categories that are of most interest to you and get affinities for those selections. For example, *Coca-Cola* and *Starbucks* were chosen in the following example.
  
    > [!div class="mx-imgBorder"]
    > ![Choose on my own](media/configure-data-enrich-profile-brands-example.png "Choose on my own")

    To add a brand or interest, in the keywords field (shown in the preceding image), type a keyword. If that keyword matches a brand or interest name in the Microsoft database, it will be saved. You can save up to five selections. If there is no match, you will get the following notice, which you can use to send a suggestion to the Customer Insights team.

    > [!div class="mx-imgBorder"]
    > ![Suggest a brand](media/configure-data-enrich-profile-suggest-brand.png "Suggest a brand")

- **Industry's top brands and categories**: For a selected industry, get the brands and interests that your total customer base, taken together, has the highest affinity for. Note that in "customer base" we refer here only to those customers whose profiles are similar to the ones defined in the **Demographic profile attributes** part.
  
## Run the enrichment process

Select **Run** at the top of the screen.

> [!div class="mx-imgBorder"]
> ![Run the enrichment process](media/configure-data-enrich-profile-choose-own.png "Run the enrichment process")

You'll see the following page as long as the enrichment algorithm is still running.

> [!div class="mx-imgBorder"]
> ![Enrichment running](media/configure-data-enrich-profile-enriching.png "Enrichment running")

To reselect your definitions and keywords, use the **Discard** button.

## Validate the enrichment process output

If the enrichment process succeeds, you'll see the following screen.

> [!div class="mx-imgBorder"]
> ![Enriched profiles](media/configure-data-enrich-profile-succeeded.png "Enriched profiles")

Use the **Enriched profiles** result to assess your enrichment definitions and keywords, and to consider whether any of them should be reconfigured.

If the enrichment process fails, you'll find the reason for that failure at the top of the screen.

> [!div class="mx-imgBorder"]
> ![Enrichment failure](media/configure-data-enrich-profile-failed.png "Enrichment failure")

## Gain richer insights into your customer base

Once you have completed the enrichment process, you have unlocked additional information on affinities for brands and interests:

1. Explore affinities histograms on the home page.

   > [!div class="mx-imgBorder"]
   > ![Affinities histograms](media/enrichment-affinities-histogram.png "Affinities histograms")

    This can be done within the **Insights** section (#1 in the preceding example). The diagrams shown in #2 present the top brand affinities and interests for your total customer base. Note that the Y-axis in those histograms represent the number of profiles who have a specific brand or category affinity.

2. Explore the **MsftAudienceIntelligence: Customer 360** entity on the **Entities** page:

   - Go to the **Entities** page.
   - Select the **MsftAudienceIntelligence: Customer 360** entity.

     > [!div class="mx-imgBorder"]
     > ![MsftAudienceIntelligence: Customer 360 entity](media/configure-data-entities-info.png "MsftAudienceIntelligence: Customer 360 entity")

   - In the preceding example, one column (see #1) presents the brands and interests that were evaluated by the enrichment algorithm.
   - Another column (see #2) presents the verticals to which these brands and interests belong.
   - The rest of the columns specify relative affinities to these brands and interests among profiles that are similar to your customers'. Note that these affinity numbers represent ranks. A rank of 1 stands for the strongest affinity, and from there, the affinity decreases as the number increases.  
   - You can also export this entity using the **Export data** button in the upper-right corner of the screen (#3).

## Next step

You might want to extract more insights using the **Segments**, **Customer Card**, and **Connectors** modules if you haven't done so. You also might want to define **Measures** and/or **Activities** for richer insights.
