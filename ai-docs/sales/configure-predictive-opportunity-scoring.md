---
title: "Configure predictive opportunity scoring for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure predictive opportunity scoring for Sales Insights"
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: a1d02708-0e40-4967-ae1a-40e9c67186c8
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Configure Predictive opportunity scoring

Predictive opportunity scoring helps users to focus on revenue generation efforts by providing scores to prioritize efforts on quality opportunities. To configure Predictive opportunity scoring, follow these steps:

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features) 

2.	Go to **Change area** and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3.  On the sitemap, select **Opportunity scoring** under **Predictive models**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Set up** from the **Predictive opportunity scoring** section to go to configuration page.

    The **Getting started** page opens.

    > [!div class="mx-imgBorder"]
    > ![Predictive opportunity scoring getting started page](media/si-admin-predictive-opportunity-scoring-getting-started-page.png "Predictive opportunity scoring getting started page")

4. Select **Create Model**.

    > [!div class="mx-imgBorder"]
    > ![Create model in Predictive opportunity scoring](media/si-admin-predictive-opportunity-scoring-create-model.png "Create model in Predictive opportunity scoring")

   Creating a model takes few minutes. You will see the progress on the screen.








1. Verify that the **Prediction Accuracy** score from **Model Outcome** matches your organizational requirements and select **Apply Model**.

    > [!div class="mx-imgBorder"]
    > ![Predictive opportunity scoring accuracy score](media/predictive-opportunity-scoring-score-accuracy.png "Predictive opportunity scoring accuracy score")<br>
    The prediction opportunity scoring is applied in your organization and users can see the opportunity scoring in their views under the **Opportunity Score** column.<br>
1. (Optional) If you are not satisfied with the **Prediction Accuracy** score, select **Retrain Model** and apply.<br>
   > [!NOTE]
   > We recommend that you train the model once the data is refreshed in your organization for better prediction accuracy scoring.
1. If you want to configure the opportunity score range, enter a minimum value of the range in the Opportunity Scoring Range.<br>

   When you change the opportunity score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change a minimum range value score for **Grade A** to 70, the maximum opportunity score range for **Grade B** changes to 69.<br>
   > [!div class="mx-imgBorder"]
   > ![Predictive opportunity scoring change maximum score for grade](media/predictive-opportunity-scoring-change-max-score.png "Predictive opportunity scoring change maximum score for grade")<br>
1. Save and apply the model.<br>
   The predictive opportunity scoring is configured and ready to use in your organization. The score refreshes every 24 hours. When you recreate a model, the application takes 24 hours to apply the new model.

> [!NOTE]
> For more information about Predictive opportunity scoring and how it can help your users, see [Convert opportunities into deals](../sales/work-predictive-opportunity-scoring.md).






