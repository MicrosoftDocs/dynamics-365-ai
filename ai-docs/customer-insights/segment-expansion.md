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

1. By default, the system suggests to include only 20% of the customers that were found to be similar with all similarity degrees. Edit this threshold as needed. As you increase this threshold, be aware that precision will decrease.

1. Select **Run** at the bottom of the page.

## View an expanded segment output

Upon clicking **Run** an ML model (binary classification) will be used to analyze your data. You can expect to see a notification at the top of the **Segment list page** until processing of the expanded segment has been completed. Once that happens, you will see your segment added to the list. 
Click **View** to view the expanded segment **Members page**. Note that the Members page for an expanded segment include two additional components:
1. A **Similarity score** column was added: The values in this column range between 0 and 1. For more information on Similarity scores visit the last section of this topic.

2. Description of the distribution of the results among the four score ranges mentioned above.

## Act on an expanded segment output

You can act on an expanded segment output in many ways that are common to other segments. Including **Exporting a segment, building a **Measure** on top of the segment, using it in **Predictions** or **Custom models**, and connecting it to **Flow**. To learn more on these mechanisms and others, visit the **Segments** topic.  

## Refresh and edit an expanded segment

In order to refresh an expanded segment, choose it on the **Segment list** page and click **Refresh** from the top action menu. Note that it result in a new ML algorithm that will process your data with the previous configurations you set up for your expansion.
Currently editing an expanded segment will also result in a new ML algorithm that will process your data. Upon the completion of the following steps, your previously created expanded segment will be deleted and replaced with a new expanded segment.

1.	Choose your expanded segment of interest within the **Segment list** page.
2.	Click **Edit** on the top action menu.
3.	Your previous selections will be shown in the **Expand segment** page and you can change any of them as needed.
4.	Click **Run** at the bottom of the page.

## Delete an expanded segment

Simply choose your expanded segment of interest from the **Segment list** page and click **Delete** from the top action menu.

## About similarity scores

The AI model gives custoemrs a score based on how similar they are to customers in your source segment. The scores range between 0.55-1 with 0.55 representing some similarity and 1 representing customers who are completely similar. Customers with scores below 0.55 are not included in the model output since a score below 0.5 represents customers who were found to be non-similar to some extent to the source segment. 
- Scores below 0.4 reflect customers the system didn’t find to be similar to the source
- Scores between 0.4 – 0.6 reflect customers the system found to be somewhat similar
- Scores between 0.6 – 0.8 reflect customers the system found to be similar
- Scores between 0.8 – 1 reflect customers the system found to be very similar