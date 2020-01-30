---
title: "Understand the configuration of premium forecasting in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Understand the configuration of premium forecasting in Dynamics 365 Sales Insights."
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

# About premium forecasting

Predictive forecasting helps sellers and managers improve their forecast accuracy by providing forecast projection based on data. To achieve this, predictive forecasting uses artificial intelligence (AI) driven models that look at historical data and the sales pipeline to predict future revenue outcome. 

## Prerequisites 

Review the following requirements before you use the premium forecast features: 

- Purchase a **Dynamics 365 Sales Insights** license or start a trial to use advanced Sales Insights features. 

- Enable forecasting. To learn more, see [Enable forecasting](/sales-enterprise/enable-forecast). 

## Features available in predictive forecasting

The following premium forecasting features are available with Sales Insights:

### Forecast predictions

Provides an AI-powered forecast that helps sellers and managers understand how much revenue their sales team could achieve. These predictions are calculated based on historical data and current sales pipeline and are available at each level of the hierarchy. A detailed breakdown is also provided. 

To verify that the predictive forecasting feature is enabled in your organization, go to **Change area** > **App settings** > **Forecast configuration** and while creating an **Org chart** based forecast, the **Prediction** column should be shown. Select the **Prediction** column to add to a forecast. To learn more, see [Choose layout and columns](/sales-enterprise/choose-layout-and-columns-forecast).

After you activate the forecast, for the first time, the predictive forecasting takes about two hours to display the data in the column.

To learn more, see [Configure a forecast in your organization](/sales-enterprise/configure-forecast)

Consider the following things before you start using predictive forecasting:

- At least 200 closed opportunities are required for the predictive forecasting model to work. For most accurate predictions, you must have at least two years' worth of closed opportunities.

    > [!NOTE]
    > Configure the **Actual Close Date** and **Actual Revenue** fields for the opportunities.

- **Prediction** column is available only for **Org chart** based forecasts.  

- Additional filters created for the forecast don't impact the outcome of predictive forecasting model.

- To optimize accuracy of the predictive forecast model, consider activating and publishing the predictive opportunity scoring. To learn more, see [Predictive opportunity scoring](configure-predictive-opportunity-scoring.md).

### Snapshots

Allows sales organizations to freeze the forecast data at a moment in time. To learn more on how to use snapshots and how deals flow between two snapshots, see [Manage snapshots for a forecast](manage-snapshots-forecast.md) and [Analyze deals flow between snapshots](analyze-deals-flow-between-snapshots.md).

### Trend chart

The **Trend** chart provides a visualization of how each forecast amount is trending overtime, comparing against the period end prediction and quota. Also, a separate predicted realization line is automatically created to project the future revenues over time.

An option **Show in Trend Chart** is available to add forecast columns to the trend chart while configuring the column in the forecast configuration. Only **Roll up** and **Calculated** column types can display in the trend chart. To learn more, see [Configure columns](/sales-enterprise/choose-layout-and-columns-forecast#configure-columns).

To understand how user use trend chart, see [Understand forecast projection through trend chart](understand-forecast-projection-through-trend-chart.md).

### Flow chart

The flow chart provides a visual representation of how the forecast changes between two moments in time. To learn more, see [Analyze deals flow between snapshots](analyze-deals-flow-between-snapshots.md).

### See also

[Manage snapshots for a forecast](manage-snapshots-forecast.md)

[Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)