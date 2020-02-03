---
title: "Analyze revenue outcome using predictive forecasting in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Analyze revenue outcome using predictive forecasting in Dynamics 365 Sales Insights."
ms.date: 02/03/2020
ms.service: 
  - "dynamics-365-sales"
ms.custom: 
  - "dyn365-sales"
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---


# Analyze revenue outcome by using predictive forecasting

Predictive forecasting helps sellers and managers improve their forecast accuracy by providing forecast projections based on data. To achieve this, predictive forecasting uses AI-driven models that look at historical data and the open sales pipeline to predict future revenue outcome.

## Prerequisites

Review the following prerequisite before you start using predictive forecasting:

  -	Ensure that the predictive forecasting feature is enabled and a forecast is configured accordingly. To learn more, see [About predictive forecasting](configure-premium-forecasting.md).

## Understand the Prediction column and details in a forecast

The **Prediction** column shows the predicted revenue for each seller and manager. Predictions are based on the **Status** field of an opportunity. To optimize the accuracy of the predictions, ensure the **Forecast Category** values are kept in sync with the **Status** field. For the out-of-the-box forecast category, a workflow ensures that when an opportunity is closed as **Won** or **Lost**, the forecast category is updated with the proper value. 

> [!NOTE]
> If there's not enough data for predictive forecasting to work, it displays an error with an empty value in the column. 

### Prediction column

Open a forecast that includes a **Prediction** column. To learn more, see [View a forecast](https://docs.microsoft.com/dynamics365/sales-enterprise/view-forecasts). 

The following screen shows an example of a **Prediction** column. 

> [!div class="mx-imgBorder"]
> ![Prediction column](media/predictive-forecasting-prediction-column.png "Prediction column")

When you hover over the information icon on the column header, the last recalculation date of the prediction is shown. Predictions are recalculated every seven days.

### Prediction details

Select a value in the prediction column to display the **Prediction details** pane.

  > [!div class="mx-imgBorder"]
  > ![Prediction column](media/predictive-forecasting-prediction-details.png "Prediction details")

The prediction details graph consists of the following values:

-	**Closed won**: Total number of opportunities that have already been closed during the current forecast period.

-	**Wins from existing deals**: Total number of existing opportunities that are predicted to close during the current forecasting period.

-	**Wins from new deals**: Total number of new opportunities that are predicted to close during the current forecasting period.

-	**Total prediction**: Total predicted amount for the current forecasting period.


### See also

[About predictive forecasting](configure-premium-forecasting.md)
