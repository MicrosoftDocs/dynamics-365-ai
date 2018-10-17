---
title: "Work with Predictive opportunity scoring feature for Dynamics 365 Customer Engagement  | MicrosoftDocs"
description: ""
keywords: ""
ms.date: 04/01/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
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

# Convert opportunities into deals

Applies to Dynamics 365 (online), version 9.0.2<br>

Predictive opportunity scoring helps you to focus on potential opportunities to achieve your sales targets. To achieve this opportunity scoring provides scores for opportunities to prioritize efforts on quality opportunities and turn them into deals. Using this score, you can identify best possible opportunities that are available for you to close deals and achieve your targets. When the score is higher, the more likely that you can convert it into deal. These opportunities are displayed in a system view—and when you select an opportunity, you can view reasons and influences of that opportunity to further analyze and build a strategy and turn the opportunity into a deal.

> [!IMPORTANT]
> To enable Predictive opportunity scoring in your organization, contact your system administrator. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure Predictive opportunity scoring](configure-enable-sales-insights-addon.md#configure-predictive-opportunity-scoring)

## Understand opportunity scoring in views

When the predictive opportunity scoring is enabled in your organization, you can use the **My Open Opportunities Scored** system view. This view gives you a list of opportunities that can be converted into win deals.

The following screen displays a typical view with a list of opportunities that consist of parameters that are used to analyze possible win deals.

> [!div class="mx-imgBorder"]
> ![My open opportunity scored view](media/my-open-opportunity-score-view.png "My open opportunity scored view")

The numbered columns are:
1. **Opportunity Score.** Specifies the value that is representative of the likelihood of the opportunity to convert into a win deal.  
2. **Opportunity Grade.** Specifies the grades of an opportunity that are categorized into A, B, C, and D with colors green, purple, yellow, and red, respectively, where Grade A (Green) is the opportunity with highest likelihood for conversion into a win deal followed by Grade B (Purple), Grade C (Yellow), and Grade D (Red).

    > [!NOTE]
    > A system administrator can define opportunity score ranges for a grade, depending on the organizational requirements.

3. **Opportunity Score Trend.** Specifies the direction in which an opportunity is trending such as **Improving** (up arrow), **Declining** (down arrow), **Steady** (right arrow), or **Not enough info**. These trends are displayed by comparing the present opportunity score with the previous score. For example, the score of an opportunity was 65 and the present score is decreased to 45, a down arrow is displayed in the **Opportunity Score Trend** column specifying that the opportunity is losing traction and needs some action from you to improve the score.

## Analyze and improve your opportunity score

In forms, you can use the **Opportunity Score** widget to see the top ten reasons that are impacting the opportunity score. This helps you to analyze and work on the opportunity to improve the score and convert it into a win deal.

The following screen displays a typical **Opportunity Score** widget with reasons that are influencing the opportunity score.

> [!div class="mx-imgBorder"]
> ![Predictive opportunity score widget](media/predictive-opportunity-scoring-widget.png "Predictive opportunity score widget")

The numbered sections are:
1. **Basic Information.** Displays the basic information of an opportunity—such as opportunity score, opportunity grade, and opportunity score trend—to help you avoid going back to the **My Open Opportunities Scored** view to see basic information.
2. **Top Reasons.** Displays the list of reason that are affecting the opportunity score. This helps you to analyze and consider the opportunity for converting into a win deal. You can also take necessary action to improve the opportunity score, such as set up meetings and follow-ups.
3. **Feedback.** Displays feedback that's provided by a user to an opportunity. You can change the feedback with an appropriate opportunity score. 
To provide feedback, select the **Chat** icon and enter the expected score and comments. To save the feedback, select **Send**.

### See also

[Configure and enable sales insights add-on](configure-enable-sales-insights-addon.md) 