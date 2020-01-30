---
title: "Understand forecast projection through trend chart in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Understand forecast projection through trend chart in Dynamics 365 Sales Insights."
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

# Understand forecast projection through trend chart

The **Trend** chart shows how each forecast amount is trending overtime, comparing against the period end prediction and quota. A separate predicted realization line is automatically created to project the future revenue over time.  

> [!NOTE]
> The **Trend** chart is available as part of predictive forecasting feature. Verify that premium forecasting is enabled for your organization. To learn more, see [About premium forecasting](configure-premium-forecasting.md).

## View trend charts

1.	Sign in to the **Sales Hub** app.

2.	At the bottom of the site map, select the **Change area** icon, and then select **Sales**.  

3.	Under **Performance**, select **Forecasts**.

    The forecast view page displays.

4.	Select the forecast and choose a forecast period for the forecast.

5.	Select **Trend** tab.

    A line chart is displayed with the comparison between the forecast categories until today.

## Understand trend chart

> [!NOTE]
> Columns available for trending can be configured in the forecast configuration. To learn more, see configure columns.

The following screenshot is an example of trend chart:

> [!div class="mx-imgBorder"]
> ![Trend chart](media/predictive-forecasting-trend-chart.png "Trend chart")

When you hover the cursor over a forecast category in the legend, the trend line of the forecast category gets highlighted.

You can also view the summary of a forecast category at a given time by placing the cursor on the trend line. The summary displays the date, forecast category, and aggregated opportunity amount.

If you don't want to view any forecast category on the chart, select the forecast category on the legend and the forecast category is grayed out. To view it again on the chart, select the forecast category.


### See also

[Analyze revenue outcome using predictive forecasting](analyze-revenue-outcome-using-predictive-forecasting.md)

[About premium forecasting](configure-premium-forecasting.md)