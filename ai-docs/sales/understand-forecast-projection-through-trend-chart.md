---
title: "Understand forecast projection through trend charts in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Understand forecast projection through trend charts in Dynamics 365 Sales Insights."
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

# Understand forecast projections by using trend charts

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]
> - Microsoft doesn't provide support for this preview feature. Microsoft Technical Support won’t be able to help you with issues or questions. Preview features aren't meant for production use and are subject to a separate [supplemental terms of use](https://go.microsoft.com/fwlink/p/?linkid=870960).

The **Trend** chart shows how each forecast amount is trending over time, comparing it against the period end prediction and quota. A separate predicted realization line is automatically created to project future revenue over time.  

> [!NOTE]
> The **Trend** chart is available as part of the predictive forecasting feature. Verify that predictive forecasting is enabled for your organization. To learn more, see [About predictive forecasting](configure-premium-forecasting.md).

## View trend charts

1.	Sign in to the Sales Hub app.

2.	At the bottom of the site map, select the **Change area** icon, and then select **Sales**.  

3.	Under **Performance**, select **Forecasts**.

4.	Select a forecast, and choose a forecast period for the forecast.

5.	Select the **Trend** tab.

    A line chart is displayed with the comparison between the forecast categories until the present day.

## Understand trend charts

> [!NOTE]
> Columns available for trending can be configured in the forecast configuration. To learn more, see [configure columns](https://docs.microsoft.com/dynamics365/sales-enterprise/choose-layout-and-columns-forecast#configure-columns).

The following screenshot shows an example of a trend chart.

> [!div class="mx-imgBorder"]
> ![Trend chart](media/predictive-forecasting-trend-chart.png "Trend chart")

When you hover over a forecast category in the legend, the trend line of the forecast category gets highlighted.

You can also view the summary of a forecast category at a given time by hovering over the trend line. The summary displays the date, forecast category, and aggregated opportunity amount.

If you don't want to view any forecast category on the chart, select the forecast category on the legend and the forecast category will be grayed out. To view it again on the chart, select the forecast category.


### See also

[Analyze revenue outcome by using predictive forecasting](analyze-revenue-outcome-using-predictive-forecasting.md)<br>
[About premium forecasting](configure-premium-forecasting.md)