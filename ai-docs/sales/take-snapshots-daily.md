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

# Take snapshots automatically

<!-- Early access preview note will be added here -->

Earlier, you could take snapshots manually only, and therefore you might miss or doesn’t have necessary sources to take the snapshot at a required point in time. Now, snapshots are taken automatically each day. 

You can enable snapshots while configuring forecasts. When configured for a forecast, the snapshots are taken only for that forecast and you can view deal flows and trend data based on the snapshots.

>[!NOTE]
>- Premium forecasting must be enabled.
>- If you disable the snapshot option for a forecast, only the previously taken snapshots are available.    

To enable the snapshots, follow these steps:

1.	While configuring a forecast, the **Snapshots** step is displayed. 

    To learn more on how to create a forecast, see [Configure forecast using custom rollup entity](https://docs.microsoft.com/dynamics365/sales-enterprise/configure-forecast-using-custom-rollup-entity)
 
    > [!div class="mx-imgBorder"]
    > ![Snapshot configuration step](media/predictive-forecasting-snapshot-configuration-step.png "Snapshot configuration step") 

2.	Select to enable the **Daily snapshots** option. The snapshots are automatically taken daily after the forecast is active. Once the forecast is active, snapshots might take few hours to get created.

    > [!div class="mx-imgBorder"]
    > ![Enable daily snapshot option](media/predictive-forecasting-snapshot-enable-daily.png "Enable daily snapshot option") 
 
>[!IMPORTANT]
>While configuring columns for a forecast, ensure that each column is unique, and the **Selector** option doesn’t have duplicates. If duplicates exist, an error is displayed stating that snapshots can’t be enabled for the forecast while activating the forecast.

### See also

[View snapshot history](view-snapshot-history.md)

[Analyze deal flows between dates](analyze-deal-flows.md)