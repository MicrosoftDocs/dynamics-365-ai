---
title: "Understand how to take snapshots daily in a forecast | MicrosoftDocs"
description: "Understand how to take snapshots daily in a forecast."
ms.date: 08/01/2020
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Take snapshot daily

<!-- Early access preview note will be added here -->

Earlier, premium forecasting lets you take the snapshots manually, and you may forget or doesn’t have necessary sources to take the snapshot at a required point in time. With the early access, predictive forecasting lets you take snapshots automatically. 

When you enable premium forecasting through Sales Insights, the option to enable snapshots is available to you while configuring a forecast. The snapshots are taken only for that forecast and allow you to create deal flows and trend data visualizations.

>[!NOTE]
>If you disable the snapshot option, snapshots are not created, and you can’t view deal flows and trend data visualizations for the forecast.

To enable the snapshots, follow these steps:

1.	While configuring a forecast, after the **Filter data** step you're proceeded to the **Snapshots** step. 

    To learn more on how to create a forecast, see [Configure forecast using custom rollup entity](https://docs.microsoft.com/dynamics365/sales-enterprise/configure-forecast-using-custom-rollup-entity)
 
    > [!div class="mx-imgBorder"]
    > ![Snapshot configuration step](media/predictive-forecasting-snapshot-configuration-step.png "Snapshot configuration step") 

2.	Select to enable the Daily snapshots option to take snapshots daily. The snapshots are automatically taken daily after the forecast is active. For each forecast, automatic snapshots are taken at six-hour time gap and help in proper utilization of application resources that are required to take snapshot.

    > [!div class="mx-imgBorder"]
    > ![Enable daily snapshot option](media/predictive-forecasting-snapshot-enable-daily.png "Enable daily snapshot option") 
 
>[!IMPORTANT]
>While configuring columns for a forecast, ensure that each column is unique, and the **Selector** option doesn’t have duplicates. If duplicates exist, an error is displayed stating that snapshots can’t be enabled for the forecast while activating the forecast.

### See also

[View snapshot history](view-snapshots-history.md)

[Analyze deal flows between dates](analyze-deal-flows.md)