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

# Configure predictive opportunity scoring

Predictive opportunity scoring uses a predictive machine learning model to calculate a score for all open opportunities. The score helps salespeople prioritize opportunities, achieve higher opportunity qualification rates, and reduce the time that it takes to qualify an opportunity.

When you configure the predictive opportunity scoring feature, the application uses out-of-the-box fields related to opportunities to generate a model with a score. Using this score, users can do the following:
 
- Identify quality opportunities and convert them into win deals.
 
- Spend time on opportunities that have low scores, and convert them into possible deals.

The predictive opportunity scoring lets you add custom fields to generate a model for predictive opportunity scoring that is accurate. The custom fields can be specific to your organization so that you can decide the impact of the outcome.

The following illustration explains how you can configure the predictive opportunity scoring.

> [!div class="mx-imgBorder"]
> ![Steps to configure predictive opportunity scoring](media/si-pos-config-steps.png "Steps to configure predictive opportunity scoring")

Before we configure the predictive opportunity scoring, let's understand the configuration page after a model is generated.

## Understand the configuration page

When a model is generated and published, the configuration page displays as shown in the following screenshot:

> [!div class="mx-imgBorder"]
> ![Configuration page](media/si-admin-predictive-opportunity-scoring-configuration-page.png "Configuration page")


Typically, you can categorize the screen into the following sections:

-	[Actions you can perform on the model](#actions-you-can-perform-on-the-model)

-	[Version details](#version-details)

-	[Opportunity score grading](#opportunity-score-grading)

### Actions you can perform on the model

Displays the actionable buttons that you can perform on the mode.

> [!div class="mx-imgBorder"]
> ![Action buttons of opportunity scoring](media/si-admin-predictive-lead-scoring-buttons.png "Action buttons of opportunity scoring")

-	**Publish**: The **Publish** button allows you to publish a model to your organization. Subsequently, users in your organization can see **My Open Opportunities Scored** system view and opportunity score widget on opportunity forms. After you publish, the **Publish** button is available only after you retrain or edit the model.

-	**Revert version**: The **Revert version** button allows you to return the model to the previous version when the retrained model is not satisfactory or not at an acceptable level of your organization's requirements. This option is available only when you retrain and the model is not published.

-	**Edit fields**: The **Edit fields** button allows you to update or add the fields that affect the prediction accuracy score. This is useful when you want to tweak the model to consider a unique business process. To learn more, see Retrain the model.

-	**Retrain Model**: The **Retrain Model** button is available only for standard model creation. You can select this option to regenerate a model with updated information that is available in your organization for improved predictive accuracy score.

### Version details

Displays the parameters with information of the model such as, version trained date, status of the version, fields used, and most influential fields. 

> [!div class="mx-imgBorder"]
> ![Version details of opportunity scoring](media/si-admin-predictive-opportunity-scoring-version-details.png "Version details of opportunity scoring")

Let’s look at these parameters in detail:

-	**Version trained on**: This parameter displays a date that lets you know when the model was last trained.

-	**Status**: This parameter lets you know the status of the model.

-	**Fields used**: This parameter lets you know the number of attributes (fields) used from the available list to generate the prediction accuracy score for the model. You can select the **Retrain with recommended fields** option to retrain the model with standard (out-of-the-box) attributes if the outcome of the trained model is not satisfactory.

    If the parameter displays **edited** corresponding to the number of fields used, specifies that the model generated is custom defined.

-	**Model performance**: This parameter displays information on the model's performance in predicting the opportunities that could convert into deals. Depending on the information, you can take appropriate action on what you want to do with the model.

    >[NOTE]
    >The range of the accuracy score is defined based on the Area Under the Curve (AUC) classification measurements.

    -	**Ready to publish**: This specifies that the model accuracy is above the range and expect that the model performance will be good. 

    -	**OK to publish**: This specifies that the model accuracy is within the range and expect that the model may have a reasonable perform.

    -	**Not ready to publish**: This specifies that the model accuracy is below the range and expect that the model performance will be bad.

-	**Retrain automatically**: This parameter allows you to retrain the model, automatically. To learn more, see [Automatically retrain](#automatic-retrain). 

-	**Most influential fields**: This parameter displays the top five attributes (fields) that are most affecting the outcome of the prediction accuracy score.

### Opportunity score grading

When a model is published, the opportunities that are in your organization's pipeline are graded according to the range defined in this section. Each opportunity in the pipeline is graded as A, B, C, or D according to the opportunity score that an opportunity has and this score is influenced by the attributes that we selected while creating the model. Opportunities that are graded as A are more likely to be converted into deals than opportunities that are graded D. 

> [!div class="mx-imgBorder"]
> ![Grading of opportunity scoring](media/si-admin-predictive-opportunity-scoring-grading.png "Grading of opportunity scoring")

You can configure the range for the grading according to your organizational requirements. When you change opportunity score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change the minimum range value score for **Grade A** to 51, the maximum opportunity score range for **Grade B** changes to 50.


## Generate system-default model 

This model is generated based on the standard attributes (fields) that are chosen by the application.  

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features). 

2.	Go to **Change area**, and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3.  On the sitemap, select **Opportunity scoring** under **Predictive models**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Set up** from the **Predictive opportunity scoring** section to go to configuration page.

    The **Predictive opportunity scoring** configuration page is displayed.

    > [!div class="mx-imgBorder"]
    > ![Predictive opportunity scoring getting started page](media/si-admin-predictive-opportunity-scoring-getting-started-page.png "Predictive opportunity scoring getting started page")

4. Select **Get started**. The application starts generating a model and a notification is displayed on the screen.

    > [!div class="mx-imgBorder"]
    > ![Model training notification](media/si-admin-predictive-opportunity-scoring-model-training-notification.png "Model training notification")

6. After the model is generated, a confirmation notification displays with the prediction accuracy score and top five fields that are influencing the score. Select **Publish** or **View details**. 

    > [!div class="mx-imgBorder"]
    > ![Model training confirmation notification](media/si-admin-predictive-opportunity-scoring-model-confirmation-notification.png "Model training confirmation notification")

    - **Publish**: Select **Publish** if the score's accuracy is at an acceptable level as per your organization's standard.

    - **View details**: Select **View details** if the score's accuracy is not at an acceptable level. You can review the details of the model and edit the fields to improve the score's accuracy. To learn more, see [Retrain the model](#retrain-a-model). 

    To learn more about the configuration page, see [Understand the configuration page](#understand-the-configuration-page).

7. Publish the model. 
 
   The prediction opportunity scoring is applied in your organization. Users can see the opportunity scoring in their views under the **Opportunity Score** column and a widget in the opportunity form.

>[!IMPORTANT]
>Adding the predictive opportunity scoring widget to a form through legacy form designer is not supported. 

> [!NOTE]
> For more information on how predictive opportunity scoring helps users, see [Convert opportunities into deals](../sales/work-predictive-opportunity-scoring.md).

## Generate custom-defined model

At times, the system-defined model may not be accurate for your organization, as your organization might not use the standard attributes for opportunities that are used to generate the model. The enhanced predictive opportunity scoring chooses custom attributes that are specific to your organization to generate a model. Also, it allows you to choose custom attributes (fields) that are used to generate the opportunity score for a model.

Follow these steps:

1. Verify that advanced Sales Insights features are enabled. To learn more, see [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features). 

2.	Go to **Change area**, and select **Sales Insights settings**.

    > [!div class="mx-imgBorder"]
    > ![Select Sales Insights settings option](media/si-admin-change-area-sales-insights-settings.png "Select Sales Insights settings option")

3.  On the sitemap, select **Opportunity scoring** under **Predictive models**.

    > [!TIP]
    > Alternatively, in the **Sales Insights settings** page, select **Set up** from the **Predictive opportunity scoring** section to go to configuration page.

    The **Predictive opportunity scoring** configuration page displays.

    > [!div class="mx-imgBorder"]
    > ![Predictive opportunity scoring getting started page](media/si-admin-predictive-opportunity-scoring-getting-started-page.png "Predictive opportunity scoring getting started page")

4. Select **Get started**. 

    The application starts generating a model, and a notification is displayed on the screen. The application uses the standard attributes to generate the model.

    > [!div class="mx-imgBorder"]
    > ![Model training notification](media/si-admin-predictive-opportunity-scoring-model-training-notification.png "Model training notification")

5. After the model is generated, a confirmation notification displays with the prediction accuracy score and top five fields that are influencing the score. Select **Publish** or **View details**. 

    > [!div class="mx-imgBorder"]
    > ![Model training confirmation notification](media/si-admin-predictive-opportunity-scoring-model-confirmation-notification.png "Model training confirmation notification")

    - **Publish**: Select **Publish** if the score's accuracy is at an acceptable level as per your organization's standard.

    - **View details**: Select **View details** if the score's accuracy is not at an acceptable level. You can review the details of the model and edit the fields to improve the score's accuracy. To learn more, see [Retrain the model](#retrain-a-model). 

6. On the **Edit model** page, select your custom attributes from **Main Entity** and **Related Entities**.

    > [!div class="mx-imgBorder"]
    > ![Edit model page](media/si-admin-predictive-opportunity-scoring-edit-model-page.png "Edit model page")

7. Select **Retrain model**. 

    The model starts to generate with the selected custom attributes, and a notification is displayed on the screen.

8. After the model is generated, publish the model.

    The prediction opportunity scoring is applied in your organization. Users can see the opportunity scoring in their views under the **Opportunity Score** column and a widget in the opportunity form.
    
>[!IMPORTANT]
>Adding the predictive opportunity scoring widget to a form through legacy form designer is not supported. 

> [!NOTE]
> For more information on how predictive opportunity scoring helps users, see [Convert opportunities into deals](../sales/work-predictive-opportunity-scoring.md).

## Retrain a model

A model is retrained when it is old or the prediction accuracy score doesn't match your organization's standards, which in turn might increases the prediction accuracy score. The application uses the latest data (opportunities) from your organization to train the model so that it can provide better accuracy of the opportunity score for your users.

>[!NOTE]
>We recommend that you train the model once the data is refreshed in your organization for better prediction accuracy scoring.

You can retrain the model [automatically](#automatic-retrain) or [manually](#manual-retrain).

### Automatic retrain

Automatic retraining allows the application to retrain a model automatically once every 15 days. This may allow the model to learn from the data and improve the prediction accuracy over time. Depending on the model’s accuracy, the application takes an appropriate decision whether to publish or ignore the retrained model.

To retrain a model automatically, go to the predictive opportunity scoring configuration page and enable **Retrain automatically**.

Here are the scenarios where the application automatically publishes the model:

-	When the accuracy of the retrained model is equal or more than 95% of the active model.

-	When the current model is more than three months old.

>[!NOTE]
>If the accuracy of the retrained model is below the range of the application’s standard, the model will not be published automatically. 

For example, model accuracy of the retrained model is good, and this specifies that the model is better compared to the current model. The retrained model will be published automatically.


### Manual retrain

1. Go to the predictive opportunity scoring configuration page, and select **Edit fields**.

2. Perform Steps 6 to 8 from [Generate custom-defined model](#generate-custom-defined-model).


### See also

[Convert opportunities into deals](../sales/work-predictive-opportunity-scoring.md)

[Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)
