---
title: "Enrich Profiles MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/14/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# Enrich profiles

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

<!--note from editor:  Is "affinities profiles" the correct term?  -->

Dynamics 365 Customer Insights enables you to consolidate data around your customers from all of your sources through the Map, Match, and Merge phases. At the same time, Customer Insights goes beyond that and puts at your fingertips additional knowledge about your customers that comes from proprietary data. This section covers the **Enrich profiles** page that can be used to unlock data on the affinities profiles similar to your customers to hundreds of brands and dozens of interest-categories. Some examples of interest-categories are *Home Appliances*, *Shoes* and *Financial Planning*.

The **Enrich profiles** page can be accessed through the app's left-side menu as well as from the **Configure data** page.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profiles.png "Text")

**Note**: Completing both the data ingestion and data configuration processes is a prerequisite to enrichment. If you don't complete one or more of those steps, you can expect to get the following notification.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile.png "Enrich profiles more info needed")

## Explore the Enrich profiles page

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-page.png "Enrich profiles page")

As shown in the preceding example, this page includes two major sections.

- The **Demographics** section, where you should make selections for at least two fields among **Date of Birth**, **Gender**, and **Zip Code**. The intent behind these selections is to focus on the specific cohort of customers for which you wish to gain knowledge around preferred brands and interests. 
- The **Brands and categories** section, where you can take one of two approaches: **Choose on my own** or **Industry's top brands and categories**. We will explore both options below.

### Make selections in the Demographics section

As mentioned earlier, you are required to make at least two selections. 

Only some formats are supported for each of the fields.

- Supported formats for **Date of Birth**: M/d/yyyy, MMMM d, yyyy-mm-dd, MMMM yyyy
- Supported formats for **Gender**: Male, Female, Unknown
- Supported formats for **Zip Code**: Should be a 5-digit US ZIP code (only US-supported at this point)

### Make selections in the Brands and categories section

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-brands.png "Enrich profiles choose brand")

First, choose one of the following options (also highlighted in the preceding image). Then, complete your selections for that option.

<!--note from editor:  Is "affinities of profiles" the correct phrasing?  -->


1. **Choose on my own**: This option allows you to choose brands and interest-categories that are of most interest to you and to get affinities of profiles similar to your customers for those selections. For example, Coca-Cola and Starbucks were chosen in the following example.
  
  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-enrich-profile-brands-example.png "Enrich profiles choose brand example")

<!--note from editor:  Below--"go to the keywords field"? -->

To add a brand or interest, type the keywords field (highlighted in blue above) and then type the keyword. If that keyword matches a brand or interest name in the Microsoft database, it will be saved. You can save up to five selections. If there is no match, you will get the following notice, which you can use to send a suggestion to the Customer Insights team.

  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-enrich-profile-suggest-brand.png "Enrich profiles suggest brand")

2. **Industry's top brands and categories**: For a selected industry, get the brands and interests that your total customer base, taken together, has the highest affinity with. Note that we use the term "customers" to refer only to those customers whose profiles match the **Demographic profile attributes**.
  
### Run the enrichment process

This can be done via **Run** at the top of the screen (shown in red).

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-choose-own.png "Enrich profiles choose own brand")

You'll see the following page as long as the enrichment algorithm is still running.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-enriching.png "Enrich profiles enriching")

You can also use the **Discard** button to reselect your definitions and keywords (shown in blue in the preceding example).

### Validate the enrichment process output

If the enrichment process succeeds, you'll see the following screen.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-succeeded.png "Enrich profiles succeeded")

Use the **Enriched profiles** figure (shown in red in the preceding example) to assess your enrichment definitions and keywords, and to consider whether any of them should be reconfigured.

If the enrichment process fails, you'll find the reason for that failure at top of the screen.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-failed.png "Enrich profiles failed")

### Gain richer insights into your customer base

Upon the completion of the enrichment process, you have unlocked additional information on affinities to brands and interests. To explore those insights:


**1. Explore affinities histograms on the home page.**

> [!div class="mx-imgBorder"] 
> ![](media/enrichment-affinities-histogram.png "Enrich affinities histograms")

This can be done within the **Insights** section (shown in red in the preceding example). The diagrams shown in blue present the top brand affinities and interests for your customer base. Note that the Y-axis in those histograms represent the number of customers who have a specific brand or category affinity.

**2. Explore the MsftAudienceIntelligence: Customer 360 entity on the Entities page**

- Go to the **Entities** page.
- Select the **MsftAudienceIntelligence: Customer 360** entity.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-entities-info.png "Text")

- In the preceding example, the column shown in blue presents the brands and interests that were evaluated by the enrichment algorithm.
- The column shown in red presents the verticals to which these brands and interests belong.
- The rest of the columns specify relative affinities to these brands and interests among profiles that are similar to your customers. Note that these affinity numbers represent ranks. A rank of 1 stands for the strongest affinity, and from there, the affinity decreases as the number increases.  

Lastly, you can also export this entity using the **Export** button in the upper-right corner of the screen.

## Next step
You might wish to extract more insights using the **Segments**, **Customer Card**, and **Connectors** modules if you haven't done so. You might also want to define **Measures** and/or **Activities** for richer insight exploration. 
