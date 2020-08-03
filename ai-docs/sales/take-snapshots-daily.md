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
<!--Do you want to change the title and description to match the H1? (That is, to say "automatically" also?) -->
<!-- Early access preview note will be added here -->

Earlier, you could only take snapshots manually, and therefore you might have missed&mdash;or lacked necessary sources to take&mdash;a snapshot that you needed. Now, snapshots can be<!--Edit okay?--> taken automatically each day. 

You can enable snapshots while configuring forecasts. When enabled, the snapshots are taken daily for that forecast and you can view deal flows and trend data based on the snapshots.

>[!NOTE]
>- Premium forecasting must be enabled for the snapshot feature.
>- You can enable or disable snapshots any time while a forecast active. When disabled, the previously taken snapshots are still available.

**To enable snapshots**

1.	While configuring a forecast, the **Snapshots** step is displayed. 

    More information: [Configure forecasts by using a custom rollup entity](https://docs.microsoft.com/dynamics365/sales-enterprise/configure-forecast-using-custom-rollup-entity)
 
    > [!div class="mx-imgBorder"]
    > ![Snapshot configuration step](media/predictive-forecasting-snapshot-configuration-step.png "Snapshot configuration step") 

2.	Set the **Daily snapshots** toggle to **Enabled**. After the forecast is active, snapshots are automatically taken daily. The initial snapshot might take a few hours to generate.

    > [!div class="mx-imgBorder"]
    > ![Enable daily snapshots](media/predictive-forecasting-snapshot-enable-daily.png "Enable daily snapshots") 
 
>[!IMPORTANT]
>While configuring columns for a forecast, ensure that each column is unique and the **Selector** option doesn't have duplicates. If duplicates exist, when you activate the forecast an error will be displayed that states that snapshots can't be enabled for the forecast.

### See also

[View snapshot history](view-snapshot-history.md)  
[Analyze deal flows between dates](analyze-deal-flows.md)  
