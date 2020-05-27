---
title: "Work with Predictive opportunity scoring feature for Dynamics 365 Sales  | MicrosoftDocs"
description: ""
keywords: ""
ms.date: 10/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: dc27cdd2-0c47-4d90-b01b-d7d37e275809
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Prioritize opportunities through scores

In a highly competitive market, it is important for you to spend time on quality opportunities to reach your sales targets. You must identify and prioritize opportunities to convert them into wins. The Predictive opportunity scoring of Dynamics 365 Sales Insights provides a scoring model to generate scores for opportunities in your pipeline. The out-of-the-box model chooses top factors that influence the score. An administrator can view and modify the top factors that influence the scores by customizing the model. To learn more, see [Generate custom-defined model](configure-predictive-opportunity-scoring.md#generate-custom-defined-model).

This model assigns a score between 0 and 100 for opportunities based on the signals from opportunities and related entities such as contact and account. Using these scores, you can identify and prioritize opportunities that have more chances of converting into wins. 

For example, say you have two opportunities - Opportunity A and Opportunity B - in your pipeline. The opportunity scoring model applies a score of 75 for Opportunity A and 55 for Opportunity B. By looking at the score, you can predict that Opportunity A has more chances of converting into a win deal and you can engage it. Also, you can further analyze why the score of Opportunity B is low by looking at the top reasons that are influencing the score and deciding how to improve this score.

> [!IMPORTANT]
> To enable Predictive opportunity scoring in your organization, contact your system administrator.
> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure Predictive opportunity scoring](configure-predictive-opportunity-scoring.md)

## Understand opportunity scoring in views

The **My Open Opportunities Scored** system view is available for you when Predictive opportunity scoring is enabled in your organization. This view provides a list of opportunities with different parameters, including opportunity score, opportunity grade, and opportunity score trend. By analyzing these parameters, you can identify and prioritize opportunities to convert into win deals.

The following screen displays a typical view that consists of columns that can be used to analyze and prioritize the opportunities.

> [!div class="mx-imgBorder"]
> ![My Open Opportunity Scored view](media/my-open-opportunity-score-view.png "My Open Opportunity Scored view")

The numbered columns are:

1. **Opportunity Score.** Specifies the value that represents the likelihood of the opportunity to convert into a deal on a scale of 1 to 100. An opportunity with score of 100 has the highest likelihood of converting into a win deal.

    >[!NOTE]
    >The model calculates the score every 24 hours, therefore, the application may take up to 24 hours to display the score for new opportunities.

1. **Opportunity Score Trend.** Specifies the direction in which an opportunity is trending such as **Improving** (up arrow), **Declining** (down arrow), **Steady** (right arrow), or **Not enough info**. These trends are displayed by comparing the present opportunity score with the previous score. For example, the score of an opportunity was 65 and the present score has decreased to 45. A down arrow is displayed in the **Opportunity Score Trend** column specifying that the opportunity is losing traction and needs some action from you to improve the score.

1. **Opportunity Grade.** Specifies a ranks or level of quality that is given to an opportunity based on the generated score. Opportunities with higher grade have more chances of converting into win deals. The grades of an opportunity are categorized into A, B, C, and D with colors green, purple, yellow, and red, respectively, where Grade A (green) is the opportunity with the highest likelihood for conversion into a win deal followed by Grade B (purple), Grade C (yellow), and Grade D (red). The system administrator can define opportunity score ranges for a grade, depending on the organizational requirements. 

## Analyze and improve your opportunity score

In forms, you can use the **Opportunity Score** widget to see the top positive and negative reasons that are influencing the score. These reasons come from the opportunity attributes and attributes from the related entities. This helps you to analyze and work on the opportunity to improve the score and convert it into a possible win deal.

The following screen displays a typical **opportunity Score** widget with reasons that are influencing the opportunity score.

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score widget](media/predictive-opportunity-scoring-widget.png "Predictive opportunity score widget")

Typically, you can categorize the screen into the following sections:

-	[Basic information](#basic-information)

-	[Top reasons](#top-reasons)

### Basic information

Displays the basic information of an opportunity—such as opportunity score, opportunity grade, and opportunity trend.

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score basic information](media/predictive-opportunity-scoring-widget-basic-information.png "Predictive opportunity score basic information")

### Top reasons

Displays the list of positive and negative reasons that are affecting the opportunity score. This helps you to analyze and consider the opportunity for converting into an opportunity. 

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score top reasons](media/predictive-opportunity-scoring-widget-top-reasons.png "Predictive opportunity score top reasons")

When you move cursor over a reason, a tool tip is displayed with an insight on what is causing the positive or negative reason to be on the top. Further, you can work on the insight and take necessary action to improve the opportunity.

In the following example, for the reason **Finance is a strong** industry, the tool tip is displayed as **64% of leads from the financial industry are qualified within 3 days**. 

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score top reasons tool tip](media/predictive-opportunity-scoring-widget-top-reasons-tool-tip.png "Predictive opportunity score top reasons tool tip")

The **opportunity score** widget displays the only top five positive and negative reasons. To view all the positive and negative reasons that are affecting the opportunity score, select **Details**. 

The **opportunity score** pane opens with a list of all score improvers (positives) and harmers (negatives) along with a graph on how the opportunity score is trending over the time.

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score details tab](media/predictive-opportunity-scoring-widget-top-reasons-details-tab.png "Predictive opportunity score details tab")

To further know about the opportunity score, such as what is opportunity score, how it works, what does grades mean, and attributes are impacting the score, select **About** tab. 

The **About** tab helps you understand what opportunity score is and how it works, along with information on how the grades are categorized in your organization by administrators under **What does it mean** and the attributes that are impacting the score in your organization under **What impacts the score**.

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score about tab](media/predictive-opportunity-scoring-widget-top-reasons-about-tab.png "Predictive opportunity score about tab")

### See also

[Configure Predictive opportunity scoring](configure-predictive-opportunity-scoring.md)
