---
title: "Enrichment of customer profiles in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Get insights from data on affinities for hundreds of brands and dozens of interest-categories in Dynamics 365 Customer Insights."
ms.date: 03/19/2020
ms.reviewer: kishorem
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Enrichment of customer profiles with brand and interest affinities

Leverage proprietary data from the Microsoft Graph to enrich your customer data with brand and interest affinities. These affinities are determined based on data from people with similar demographics to your customers. This information helps you to better understand and segment your customers based on their affinities to specific brands and interests.

In Customer Insights, go to **Data** > **Enrichment** to configure and view the data.

:::image type="content" source="media/enrichment-page.png" alt-text="Enrichment page with configuraiton options":::

## About Microsoft Graph

We use our proprietary online search data from the Microsoft Graph to determine affinities for brands and interests across various demographic segments (defined by age, gender and/or location). The online search volume for a given brand or interest is used to determine how much affinity a given demographic segment has to that brand or interest, relative to other demographic segments.

[Learn more about Microsoft Graph](https://docs.microsoft.com/graph/overview).

## Affinity score and confidence

The **affinity score** is calculated on a 100-point scale, with 100 representing the segment that has the highest affinity for a brand or interest.

The **affinity confidence** is also on a 100-point scale indicating the system's confidence level for a given segment having affinity for the brand or interest. Confidence level is based on the segment size and the segment granularity. Segment size is determined by the amount of data we have for a given segment. Segment granularity is determined by how many attributes (age, gender, location) were used on a given profile.

We don't normalize the scores for your dataset. Consequently, you may not see all possible affinity score values for your dataset. For example, there may be no enriched customer profile with an affinity score of 100 in your data if no customers exist in the demographic segment that scored 100 for a given brand or interest.

> [!TIP]
> When [creating segments](pm-segments.md) using affinity scores, review the distribution of affinity scores for your dataset before deciding on the appropriate score thresholds. For example, an affinity score of 10 can be considered significant in a dataset that has a highest affinity score of only 25 for a given brand or interest.

## Configure Enrichment

Configuring brands and interests enrichment consists of two steps:

1. **Define your brands and interests**

   Select one of the following options:
   - **Industry**: Choose your industry, and the system automatically identifies the top brands and interests relevant to your industry and enriches your customer data with them.
   - **Choose your own**: Select up to five items from an extensive list of brands and interests that are most important to your organization to enrich your customer data with.

   To add a brand or interest, start typing in the corresponding input area to get suggestions based on matching terms. If we don't list a brand or interest you are looking for, send us feedback using the **Suggest** link.

2. **Map your fields**

   Map fields from your unified customer entity to at least two attributes. This defines the demographic segment you want us to use for enriching your customer data. Select **Edit** to define the mapping of the fields and select **Apply** when you're done. Select **Save** to finalize the field mapping.

   The following formats and values are supported:
   - **Date of Birth**: m/d/yyyy, mmmm d, yyyy-mm-dd, mmmm yyyy
   - **Gender**: Male, Female, Unknown
   - **Zip Code**: 5-digit US ZIP Code (only supported for the United States)
   - **State**: 2-letter abbreviation (only supported for the United States)

:::image type="content" source="media/enrichment-add-data.png" alt-text="Add data pane for data enrichment":::

## Run enrichment

You can run the enrichment after configuring brands, interests, and the field mapping for demographics. To start the process, select **Run** on the **Data** > **Enrichment** page. Additionally, you can let the system run the enrichment automatically as part of a scheduled refresh.
Depending on the size of your customer data, it can take several minutes for an enrichment run to complete.

## Enrichment results

Once the enrichment run has successfully completed, you can review the total number of enriched customers, as well as a breakdown of brands and interests in the enriched customer profiles.

:::image type="content" source="media/enrichment-preview.png" alt-text="Preview of results after running the enrichment process":::

You can also see the enriched data by selecting **View enriched data** in the chart. Enriched data for brands can be found in the **BrandAffinityFromMicrosoft** entity, while data for interests can be found in **InterestAffinityFromMicrosoft**. You'll also find these entities listed in the **Enrichment** group in **Data** > **Entities**.

## See enrichment data on the customer card

Brand and interest affinities can also be viewed on individual customer cards. Go to **Customers** and select a customer profile. In the customer card, you'll find charts for the brands and interests that people in that customer's demographic profile have affinity for.

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Customer card with enriched data":::

## Next steps

Consider extracting more insights and powering your business processes by leveraging your enriched customer data. Create [Segments](pm-segments.md), [Measures](pm-measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.
