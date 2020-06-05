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

Actions you can take with your insights using the options in the command bar:

- **Back** to go the list of insights
- **Refresh** to run the analysis again
- **Delete** to remove this insight



Next steps 
With segment overlap you can gain further insights into your customer base. Based on those insights you may want to create a new segment that captures one or more of the overlaps you have generated. Moreover, you can utilize the second type of analysis, Segment differentiators, to further understand what differentiates one of the segments you have analyzed from the rest of your customers or from another segment of interest. 
