---
title: "Enrich Profiles MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/21/2019
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
# Enrich Profiles

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Customer Insights enables you to consolidate data around your customers from all of your sources through the *Map*, *Match* and *Merge* phases. At the same time, Customer Insights goes beyond that and puts at your fingertips additional knowledge about your customers that comes from proprietary data. This section covers the **Enrich Profiles** page that can be used to unlock data on the affinities profiles similar to your customers have to hundreds of brands and dozens of interest-categories (some examples for interest-categories are *Home Appliances*, *Shoes* and *Financial loans* but there are many others too).

The **Enrich Profiles** page can be accessed through the app left-side menu as well as from the **Configure Data** page:

// missing 1

**Note**: Completing both the *Data Ingestion* and *Data Configuration* processes is a prerequisite to enrichment. If you didn't complete one or more of those steps, you can expect to get the following notification.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile.png "Enrich profiles more info needed")

## Explore the Enrich Profiles page

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-page.png "Enrich profiles page")

As shown above, this page includes two major sections:

- The **Demographics** section, where you should make selections for at least two fields among **Date of Birth**, **Gender**, and **Zip Code**. The intent behind these selections is to focus on the specific cohort of customers for which you wish to gain knowledge around preferred brands and interests. 
- The **Brands and Categories** section, where you can take one of two approaches: **Choose on my own** or **Industry's top Brands and Categories**. We will explore both options below.

### Make selections on the *Demographics* section

As mentioned earlier, you are required to make at least two selections. 

Only some formats are supported for each of the fields.

- Supported formats for **Date of Birth**: M/d/yyyy, MMMM d, yyyy-mm-dd, MMMM yyyy
- Supported formats for **Gender**: Male, Female, Unknown
- Supported formats for **Zip Code**: Should be a 5-digit US zip code (only US supported at this point)

### Make selections on the *Brands and Categories* section

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-brands.png "Enrich profiles choose brand")

First choose one of the following options (also highlighted in the image above). Then complete your selections for that option.

1. **Choose on my own**: This option allows you to choose brands and interest-categories that are of most interest to you and get affinities of profiles similar to your customers for those selections. For example, *Coca-Cola* and *Starbucks* were chosen in the example below.
  
  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-enrich-profile-brands-example.png "Enrich profiles choose brand example")

To add a brand or interest, type the keywords field (highlighted in blue above) and then type the keyword. If that keyword matches a brand or interest name in the Microsoft database it will be saved. **You can save up to five selections.** If there is no match, you will get the following notice which you can use to send a suggestion to the Customer Insights team:

  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-enrich-profile-suggest-brand.png "Enrich profiles suggest brand")

2. **Industry's top brands and categories**: Get the brands and interests which your total customer base, taken together, has the highest affinity with. Note that in *Customers* we refer here only to the customers you have chosen in the **Demographics** section. In the example below, **Home&Garden** was chosen as an industry.
  
<!-- // enrich 6 - still missing

Here is the list of supported industries: To complete -->
  
### Run the Enrichment process

That can be easily done via **Run** at the top of the screen (shown in red):

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-choose-own.png "Enrich profiles choose own brand")

You'll see the following page as long as the Enrichment algorithm is still running:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-enriching.png "Enrich profiles enriching")

You can also use the **Discard** button to reselect your definitions and keywords (shown in blue above).

### Validate the Enrichment process output

If the Enrichment process succeeded, you'll see the following screen.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-succeeded.png "Enrich profiles succeeded")

Utilize the **Enriched Profiles** figure (shown in red above) to assess your enrichment definitions and keywords, and to consider if any of them should be reconfigured.

If the Enrichment process failed, however, you'll find the reason for that failure at top of the screen.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-enrich-profile-failed.png "Enrich profiles failed")

### Gain Richer Insights on your Customer Base
Upon the completion of the Enrichment process, you have unlocked additional information on affinities to brands and interests. To explore those insights:
1. Go to the entities screen
2. Select the **MsftAudienceIntelligence: Customer 360** entity

// missing 2

- Shown above in blue, this column presents the brands and interests that were evaluated by the enrichment algorithm.
- Shown in red, this column presents the verticals to which these brands and interests belong
- The rest of the columns specify relative affinities to these brands and interests among profiles that are similar to your customers. **Note that these affinity numbers represent ranks:** Hence a rank of 1 stands for the strongest affinity and from there the affinity decreases as the number increases.  

Lastly, you can also **Export** this entity as shown below:

// missing 3

## Next Step
You may wish to extract more insights using the **Segments**, **Customer Card** and **Connectors** modules if you haven't done so. You may also want to define **Measures** and/or **Activities** for richer insight exploration. 
