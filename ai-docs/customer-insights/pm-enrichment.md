---
title: "Enrichment | Microsoft Docs"
description: "Get insights from data on affinities for hundreds of brands and dozens of interest-categories in Dynamics 365 Customer Insights."
ms.date: 03/17/2020
ms.reviewer: kishorem
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Enrichment

Leverage proprietary data from the Microsoft Graph to enrich your customer data with brands and interests affinities. These affinities are determined based on data from people with similar demographics to your customers. This information helps you to better understand and segment your customers in terms of their affinities to specific brands and interests.

In Customer Insights, go to **Data** > **Enrichment** to configure and view the data.

## About Microsoft Graph

We use our proprietary online search data from the Microsoft Graph to determine affinities for the brands and interests across various demographic segments (defined by age, gender and/or location). The online search volume for a given brand or interest is used to determine whether and how much affinity a given demographic segment has to that brand or interest, relative to other demographic segments.

[Learn more about Microsoft Graph](https://docs.microsoft.com/graph/overview).

## Affinity score and confidence

The **affinity score** is calculated on a 100-point scale, with 100 representing the segment that has the highest affinity for a brand or interest.

The **affinity confidence** is also on a 100-point scale indicating the system's confidence level for a given segment having affinity for the brand or interest. Confidence level is based on the segment size and the segment granularity. This related to the amount of data we have for a given segment and how many attributes (age, gender, location) were used on a given profile.   
We don't normalize the scores for your dataset. Consequently, you may not see all possible affinity score values for your dataset. For example, there may be no enriched customer profile with an affinity score of 100 in your data if no customers exist that belongs to the demographic segment that scored 100 for a given brand or interest.

> [!TIP]
> When [creating segments](pm-segments.md) using affinity scores, review the distribution of affinity scores for your dataset before deciding on the appropriate score thresholds. For example, an affinity score of 10 can be considered significant in a dataset that has a highest affinity score of only 25 for a given brand or interest.

## Configure Enrichment

Configuring the brands and interests enrichment consists of two steps.

1. **Define your brands and interests**
   Select one of the following options.
   - **Industry**: Choose your industry and the system automatically identifies the top brands and interests relevant to your industry and enrich your customer data with them
   - **Choose your own**: Select up to 5 items from the extensive list of brands and interests that are most important to your organization to enrich your customer data with

   To add a brand or interest, start typing in the corresponding input area to get suggestions based on matching terms. If we don't list a brand or interest you are looking for, send us feedback using the **Suggest** link.

2. **Map your fields**
   Map fields from your customer entity to at least two attributes. This defines the demographic segment you want us to use for enriching your customer data. Select **Edit** to define the mapping of the fields.

   The following formats and values are supported:
   - Date of Birth: m/d/yyyy, mmmm d, yyyy-mm-dd, mmmm yyyy
   - Gender: Male, Female, Unknown
   - Zip Code: 5-digit US ZIP Code (only supported for the United States)
   - State: 2-letter abbreviation (only supported for the United States)

## Explore the Enrichment page

The **Enrichment** page includes two major sections where you'll define the parameters to enrich your data.

![Screenshot of the Enrichment page in Customer Insights](media/configure-data-enrich-profile-page.png)

- **Demographics**: Define demographics for a specific group of profile types for which you want to gain insights around preferred brands and interests.

- **Brands and categories**: Select whether Customer Insights delivers insights about groups of profiles based on your own selections, or based on industry trends.

## Demographics section

You'll need to define the values for at least two fields to enrich your unified customer profiles.

The following formats and values are supported:

- **Date of Birth**: m/d/yyyy, mmmm d, yyyy-mm-dd, mmmm yyyy
- **Gender**: Male, Female, Unknown
- **Zip Code**: 5-digit US ZIP Code (only supported for the US)

## Brands and categories section

Choose one of the following options. Then, provide the information for that option.

- **Choose on my own**: This option lets you choose brands and categories of interest to get affinities for those selections.

   To add a brand or category, enter a keyword in the corresponding input field. The system will search for a keyword match in the underlying database. If a match isn't found, you can send a suggestion to the Customer Insights team. You can add up to five brands or categories.

- **Industry's top brands and categories**: For a selected industry, get the brands and interests that your customer base has the highest affinity for. *Customer base* refers to customer profiles that are similar to the ones defined in the **Demographics** section.
  
## Run the enrichment process

After defining or updating values on the **Enrichment** page, you need to select **Run** in the page header to start the enrichment process. It can take a few minutes to run the enrichment algorithm.

## Validate the enrichment process output

After the enrichment process completes, you'll find the number of **Enriched profiles** on the **Enrichment** page.

> [!div class="mx-imgBorder"]
> ![Enriched profiles](media/configure-data-enrich-profile-succeeded.png "Enriched profiles")

If the enrichment process fails, you'll find the reason at the top of the screen.

## Gain richer insights into your customer base

After completing the enrichment process, you'll find additional information on affinities for brands and interests.

1. Go to the **Home** page and find affinity bar charts in the **Insights** section.

2. Go to **Data** > **Entities** and select the **MsftAudienceIntelligence: Customer Insights** entity.

   > [!div class="mx-imgBorder"]
   > ![MsftAudienceIntelligence: Customer Insights entity](media/configure-data-entities-info.png "MsftAudienceIntelligence: Customer Insights entity")

   - The **Segment** column lists the brands and interests that were evaluated by the enrichment algorithm.
   - The **IndustryVertical** column lists the industry to which the brands and interests belong.
   - The rest of the columns specify relative affinities to these brands and interests among profiles that are similar to your customers'. The affinity numbers represent ranks, with a rank of "1" standing for the strongest affinity.
   - To export this entity, select **Download as CSV**.

## Next step

Consider extracting more insights using the **Segments**, **Customer Card**, and **Connectors** modules if you haven't done so. You also might want to define **Measures** or **Activities** for richer insights.
