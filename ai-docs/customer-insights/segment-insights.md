---
title: "Segment insights in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Get insights on existing segments in Customer Insights."
ms.date: 06/05/2020
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
ms.reviewer: jimsonc
manager: shellyha
---

# Segments insights (preview)

Discover additional information and insights around your existing segments. Find out what differentiates a segment from other groups of customers or what they have in common.

## Segment overlap

Segment overlap analysis shows how many and which customers are common to two or more segments. For example, how a segment with high spenders overlaps with a segment that contains customers that are satisfied with yor service or product.
You can also analyze how the overlap changes for specific attributes. For example, by drilling down to a specific city.

### Run an overlap analysis

1. Go to **Segments** and select the **Insights (preview)** tab.

1. Select **New** and choose the **Overlap** option in the **Choose Insight Type** pane.

1. Choose the segments of interest and select **Next**.

1. Optionally, choose one or more fields of interest to analyze overlaps for every possible field value and select **Next**.

1. Provide a name for you overlap analysis, an optional display name, and a description.

1. Select **Save** to start the analysis. The overlap analysis is ready when the status changes from Refreshing to Successful.

### View and optimize an overlap analysis

After completing the analysis, you find details on this insight on **Segments** > **Insights (preview)**.

Select an insight to see the analysis results:

- The number of members who overlap between the segments selected for analysis.
- The number of member who are included only in one of the segments but not in the rest of the segments.
- If you selected fields while configuring the overlap analysis, you'll find them in the corresponding tabs. You can use the filter drop-down to select any attribute level of interest and the table at the bottom will show the corresponding data.

## Segment differentiators analysis

Segment differentiators help you find out what differentiates a segment from the rest of your customers or from another segment. You just have to select a segment and the system will identify profile attributes and measures that distinguish the selected segment.

### Run a differentiator analysis

1. Go to **Segments** and select the **Insights (preview)** tab.

1. Select **New** and choose the **Overlap** option in the **Choose Insight Type** pane.

1. Choose the segment you want to analyze as **Primary segment** and select **Next**.

1. Choose **All customers** or a **Secondary segment** to compare your primary segment with and select **Next**.

1. Optionally, choose one or more fields of interest to focus the analysis around specific attributes instead of looking at all attributes and select **Next**.

1. Provide a name for you overlap analysis, an optional display name, and a description.

1. Select **Save** to start the analysis. The overlap analysis is ready when the status changes from Refreshing to Successful.

### View and optimize a differentiators analysis

After completing the analysis, you find details on this insight on **Segments** > **Insights (preview)**.

Select an insight to see the analysis results. A differentiator analysis includes two tabs. The **Attributes** tab lists profile attributes considered as differentiators. The **Measures** tab lists measures considered as differentiators. Each tab includes the following details:

- Ranked list of differentiators, sorted by difference score.
- The **Difference score** for each differentiator. The difference score represents the degree of difference of an attribute between two segments. The higher the difference score, the more the attributes differ between the two segments. Select any of the scores to open the **Difference score** pane with the distributions of values for that attribute across the two compared segments.

## Manage segment insights

You can use the following options on your insights from the command bar:

- **Back** to return the list of insights
- **Refresh** to run the analysis again
- **Delete** to remove this insight
