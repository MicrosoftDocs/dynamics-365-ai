---
title: "Work with Predictive lead scoring feature for Dynamics 365 Sales  | MicrosoftDocs"
description: ""
ms.date: 10/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: f5f685e2-ea1b-4c1c-8a68-857160e22fb3
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Prioritize leads through scores

In a highly competitive market, it is important for you to spend time on quality leads to reach your sales targets. You must identify and prioritize leads to convert them onto opportunities. The predictive lead scoring of Dynamics 365 Sales Insights provides a scoring model to generate scores for leads that are available for you in your pipeline. The out-of-the-box model chooses top factors that influence the score. An administrator can view and modify the top factors that influence the scores by customizing the model. To learn more, see [Generate custom-defined model](configure-predictive-lead-scoring.md#generate-custom-defined-model).

This model assigns a score between 0 to 100 for leads based on the signals from leads and related entities such as contact and account. Using these scores, you can identify and prioritize leads that have more chances of converting into opportunities. 

For example, say you have two leads - Lead A and Lead B - in your pipeline. The lead scoring model applies a score of 80 for Lead A and 50 for Lead B. By looking at the score, you can predict that Lead A has more chances of converting into an opportunity and you can engage it. Also, you can further analyze why the score of Lead B is low by looking at the top reasons influencing the score and deciding whether to improve this score.
 
> [!IMPORTANT]
> To enable Predictive lead scoring in your organization, contact your system administrator.
> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configure Predictive lead scoring](configure-predictive-lead-scoring.md)

## Understand Predictive lead scoring in views

The **My Open Leads Scored** system view is available when Predictive lead scoring is enabled in your organization. This view provides a list of leads with different parameters including lead score, lead grade, and lead score trend. By analyzing these parameters, you can  identify and prioritize leads to convert into opportunities.

The following screen displays a typical view that consists of columns that can be used to analyze and prioritize the leads.

> [!div class="mx-imgBorder"]
> ![My Open Leads Scored view](media/my-open-lead-score-view.png "My Open Leads Scored view")

The numbered columns are:

1.	**Lead Score.** Specifies the value that represents the likelihood of the lead to convert into an opportunity on a scale of 1 to 100. A lead with a score of 100 has the highest likelihood of converting into an opportunity.

2.	**Lead Grade.** Specifies a ranks or level of quality that is given to a lead based on the generated score. Leads with higher grade have more chances of converting into opportunities. The grades of a lead are categorized into A, B, C, and D with colors green, purple, yellow, and red, respectively, where Grade A (green) is the lead with the highest likelihood for conversion into an opportunity followed by Grade B (purple), Grade C (yellow), and Grade D (red). System administrators can define lead score ranges for a grade, depending on your organizational requirements.

3. **Lead Score Trend.** Specifies the direction in which a lead is trending such as **Improving** (up arrow), **Declining** (down arrow), **Steady** (right arrow), or **Not enough info**. These trends are displayed by comparing the present lead score with the previous score. For example, the score of a lead was 65 and the present score is decreased to 45. A down arrow is displayed in the **Lead Score Trend** column specifying that the lead is losing traction and needs some action from you to improve the score. 
 
## Analyze and improve your lead score

In forms, you can use the **Lead Score** widget to see the top 10 reasons that are influencing the score. These reasons come from the lead attributes and attributes from the related entities. This helps you to analyze and work on the lead to improve the score and convert it into a possible opportunity. 

The following screen displays a typical Lead Score widget with reasons that are influencing the lead score. 

> [!div class="mx-imgBorder"]
> ![Predictive lead score widget](media/predictive-lead-scoring-widget.png "Predictive lead score widget")

The numbered sections are:

1.	**Basic Information.** Displays the basic information of a lead—such as lead score, lead grade, and lead score trend—to help you avoid going back to the My Open Leads Scored view to see basic information.

2.	**Top Reasons.** Displays the list of reasons that are affecting the lead score. This helps you to analyze and consider the lead for converting into an opportunity. You can also take necessary actions to improve the lead score, such as set up meetings and follow-ups.

3.	**Feedback.** Displays feedback that's provided by a user to a lead. You can change the feedback with an appropriate lead score. To provide feedback, select the **Chat** icon and enter the expected score and comments. To save the feedback, select **Send**.

### See also

[Configure Predictive lead scoring](configure-predictive-lead-scoring.md)
