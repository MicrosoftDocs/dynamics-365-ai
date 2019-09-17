---
title: "Configure predictive lead scoring for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure predictive lead scoring for Sales Insights"
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 8660ca75-c63c-495d-a1a6-d3a0cd36f7cb
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Configure Predictive lead scoring

Predictive lead scoring helps users to focus on revenue generation efforts by providing scores to prioritize efforts on quality leads. To configure Predictive lead scoring, follow these steps:

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features) 

2.	Go to **Change area** and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3.  On the sitemap, select **Lead scoring** under **Predictive models** to go to **Manage insight cards** page.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Set up** from the **Predictive lead scoring** section to go to **Manage insight cards** page.

1. On the **Overview** tab, select **Configuration** from the **Predictive lead scoring** section.
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring configuration](media/predictive-lead-scoring-configuration.png "Predictive lead scoring configuration")<br>

   > [!NOTE]
   > You can also select the **Predictive lead scoring** tab.

   The configuration page opens.
3. Select **Create Model**.
    > [!div class="mx-imgBorder"]
    > ![Create model in Predictive lead scoring](media/predictive-lead-scoring-create-model.png "Create model in Predictive lead scoring")<br>

   Creating a model takes a few minutes. You will see the progress on the screen.<br>
1. Verify that the **Prediction Accuracy** score from **Model Outcome** matches your organizational requirements and select **Apply Model**.
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring accuracy score](media/predictive-lead-scoring-score-accuracy.png "Predictive lead scoring accuracy score")<br>
  
    The prediction lead scoring is applied in your organization and users can see the lead scoring in their views under the **Lead Score** column.<br>
1. (Optional) If you are not satisfied with the **Prediction Accuracy** score, select **Retrain Model** and apply.<br>
   
   > [!NOTE]
   > We recommend that you train the model once the data is refreshed in your organization for better prediction accuracy scoring.
   
1. If you want to configure the lead score range, enter a minimum value of the range in the **Lead Scoring Range**.<br>

   When you change lead score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change the minimum range value score for **Grade A** to 51, the maximum lead score range for **Grade B** changes to 50.
   
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring change maximum score for grade](media/predictive-lead-scoring-change-max-score.png "Predictive lead scoring change maximum score for grade")<br>
1. Save and apply the model.<br>
   The predictive lead scoring is configured and ready to use in your organization. The score refreshes every 24 hours. When you recreate a model, the application takes 24 hours to apply the new model.

> [!NOTE]
> For more information about Predictive lead scoring and how it can help your users, see [Convert leads into opportunities](../sales/work-predictive-lead-scoring.md).





















