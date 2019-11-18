---
title: "Configure predictive lead scoring for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to configure predictive lead scoring for Sales Insights"
ms.date: 12/02/2019
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

Predictive lead scoring helps users to focus on revenue generation efforts by providing scores for the leads based on which users can prioitize thier leads. As an administrator, when you configure the predictive lead scoring feature, the system uses standard (out-of-the-box) fields related to leads to generate a model with a score. Using this score, users can do the following:
 
- Identify quality leads and convert them into opportunities.
 
- Spend time on leads that have low score, and convert them into possible opportunities.

The enhanced predictive lead scoring lets you add custom fields to generate a model for predictive lead scoring that is accurate. The custom fields could be specific to your organization so that you can decide the impact of the outcome. 

The feature is available as preview, and you must enable the preview to configure the enhanced model. The following illustration explains how you can configure the predictive lead scoring:

> [!div class="mx-imgBorder"]
> ![Steps to configure predictive lead scoring](media/si-pls-config-steps.png "Steps to configure predictive lead scoring")


## Create default system model 

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features) 

2.	Go to **Change area** and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3.  On the sitemap, select **Lead scoring** under **Predictive models**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Set up** from the **Predictive lead scoring** section to go to configuration page.

    The **predictive lead scoring** configuration page opens.

    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring getting started page](media/si-admin-predictive-lead-scoring-getting-started-page.png "Predictive lead scoring getting started page")

4. Select **Get started** and a pop up dialog opens to enable the preview.

    > [!div class="mx-imgBorder"]
    > ![Preview notification pop up window](media/si-admin-predictive-lead-scoring-preview-notification.png "Preview notification pop up window")

5. Select **Continue without preview**. The application starts generating a model and a notification is displayed on the screen.

    > [!div class="mx-imgBorder"]
    > ![Model training notification](media/si-admin-predictive-lead-scoring-model-training-notification.png "Model training notification")

6. After the model is generated, a confirmation notification displays that displays prediction accuracy score and top five fields that are influencing the score. Select **Publish** or **View details**. 

    > [!div class="mx-imgBorder"]
    > ![Model training confirmation notification](media/si-admin-predictive-lead-scoring-model-confirmation-notification.png "Model training confirmation notification")

    - **Publish**: Select **Publish** if the score's accuracy is at an acceptable level as per your organization's standard.

    - **View details**: Select **View details** if the score's accuracy is not at an acceptable level. You can review the details of the model and edit the fields to improve the score's accuracy. To learn more, see [Retrain the model](#retrain-the-model). 

## Create custom defined model









4. Select **Create Model**.

    > [!div class="mx-imgBorder"]
    > ![Create model in Predictive lead scoring](media/si-admin-predictive-lead-scoring-create-model.png "Create model in Predictive lead scoring")

   Creating a model takes a few minutes. You will see the progress on the screen.

5. Verify that the **Prediction Accuracy** score matches your organizational requirements and select **Apply Model**.

    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring accuracy score](media/si-admin-predictive-lead-scoring-score-accuracy.png "Predictive lead scoring accuracy score")
  
    The prediction lead scoring is applied in your organization and users can see the lead scoring in their views under the **Lead Score** column.

6. (Optional) If you are not satisfied with the **Prediction Accuracy** score, select **Discard Model** to discard the current model. Select **Retrain Model** to create a updated model and then select **Apply**.
   
   > [!NOTE]
   > We recommend that you train the model once the data is refreshed in your organization for better prediction accuracy scoring.
   
7. If you want to configure the lead score range, enter a minimum value of the range in the **Lead score range**.

   When you change lead score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change the minimum range value score for **Grade A** to 51, the maximum lead score range for **Grade B** changes to 50.
   
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring change maximum score for grade](media/si-admin-predictive-lead-scoring-change-max-score.png "Predictive lead scoring change maximum score for grade")

8. Save and apply the model.

   The predictive lead scoring is configured and ready to use in your organization. The score refreshes every 24 hours. When you recreate a model, the application takes 24 hours to apply the new model.


### See also

[Convert leads into opportunities](../sales/work-predictive-lead-scoring.md)

[Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)