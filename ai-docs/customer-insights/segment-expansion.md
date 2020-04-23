---
title: "Expand existing segments with AI | Microsoft Docs"
description: "Find similar customer segments with artificial intelligence."
ms.date: 04/21/2020
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
ms.reviewer: nimagen
manager: shellyha
---

# Expand segments (preview)

*Segment expansion* lets you find similar customers in your customer base using artificial intelligence. You need to have at least one segment created to use this feature. Expanding segments help find customers that are similar to an **existing** segment.

> [!NOTE]
> Segment expansion uses automated means to evaluate data and make predictions based on that data, and therefore has the capability to be used as a method of profiling, as that term is defined by the General Data Protection Regulation (“GDPR”). Customer’s use of this feature to process data may be subject to GDPR or other laws or regulations. You are responsible for ensuring that your use of Customer Insights, including predictions, complies with all applicable laws and regulations, including laws related to privacy, personal data, biometric data, data protection, and confidentiality of communications.

## Expand an existing segment

1. In Customer Insights, go to **Segments** and select the segment you want to expand. That's your *source segment*.

1. In the action bar, select **Expand segment**.

1. Review the suggested name for your new segment and change it if necessary.

1. Review the fields that define your new segment. These fields define the basis on which the system will try to find similar customers to your source segment. The system will select recommended fields by default.
  Fields that can significantly decrease the model performance are automatically excluded:
  
  - Fields with the following data types: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType
  - Fields with a cardinality (the number of elements in a field) of less than 2 or more than 30

1. Choose if you want to include **All customers** or only those in a **Specific existing segment** in your new segment.

1. Exclude customers in your source segment by selecting the **Exclude everyone in source segment** checkbox.

1. By default, the system suggests to include only 20% of the customers that were found to be similar with all similarity degrees. Edit this threshold as needed. Increasing this threshold will decrease precision.

1. Select **Run** at the bottom of the page to start a binary classification task (a method of machine learning) which analyzes the dataset.

## View an expanded segment output

After processing the expanded segment, you'll find the new segment listed on the **Segments** page.

Select **View** in the action bar to open the segment details of the expanded segment. This view contains information about the distribution of the results between the four score ranges of the [similarity score](#about-similarity-scores). You'll also find the similarity score values in the **Segment members preview**.

## Use the output of an expanded segment

You can [work with the output of an expanded segment](pm-segments.md) similar to other segments. For example, export the segment, build a measure, etc.

## Refresh and edit an expanded segment

To refresh an expanded segment, select it on the **Segments** page and select **Refresh** in the action bar.

Editing an expanded segment results in a new run to process your data. The previously created expanded segment gets replaced with the new expanded segment.    
To edit an expanded segment. select it on the **Segments** page and select **Edit** in the action bar. Apply your changes and select **Run** to start the processing.

## Delete an expanded segment

Select the segment on the **Segments** page and select **Delete** in the action bar. Then, confirm your deletion.

## About similarity scores

The binary classification machine learning model assigns a score to customers in the expanded segment, based on how similar they are to customers in the source segment.

- Similarity scores below 0.4 are customers the system classified as *not similar* to customers in the source segment
- Similarity scores between 0.4 – 0.6 are classified as *somewhat similar*
- Similarity scores between 0.6 – 0.8 are classified as *similar*
- Similarity scores between 0.8 – 1 are customers the system classified as *very similar*

Customers with similarity scores below 0.55 are not included in the model output because they are not considered similar enough to the source segment.
