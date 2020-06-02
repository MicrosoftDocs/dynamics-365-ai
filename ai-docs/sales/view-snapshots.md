---
title: "Understand how to view snapshots for a forecast in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Understand how to view snapshots for a forecast in Dynamics 365 Sales Insights"
ms.date: 06/01/2020
ms.service: 
  - "dynamics-365-sales"
ms.custom: 
  - "dyn365-sales"
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# View snapshots

Viewing a snapshot allows you to see and understand the data of the forecast at the moment in time when it's taken including the underlying opportunities. Also, you can compare and understand the data between your current forecast and snapshot on how the forecast is doing. 


**To view snapshots**

1.	Sign in to the Sales Hub app and go to **Performance** > **Forecasts**.

2.	Select the forecast for which you want to view the snapshots.

3.	Select **Snapshot history**. 

    > [!div class="mx-imgBorder"]
    > ![Select snapshot history](media/predictive-forecasting-select-snapshot-history.png "Select snapshot history")

    A list of snapshot that is available for the selected forecast is displayed in the **Snapshot history** pane.
    
    > [!div class="mx-imgBorder"]
    > ![Snapshot history pane](media/predictive-forecasting-snapshot-history-pane.png "Snapshot history pane")

4.	Select a snapshot to view. In this example, we're selecting **Mar18-1** snapshot and displayed as shown in the following image:

    > [!div class="mx-imgBorder"]
    > ![View a snapshot](media/predictive-forecasting-select-snapshot-to-view.png "View a snapshot")

    >[!NOTE]
    >The data displayed in the snapshot is view only and can't be modified.

    You can select a column and see the underlying opportunities that are defining the value of the column at that point in time. For example, we're selecting Kenny Smith's Committed column and the underlying opportunities that are contributing the value in the **Committed** column at that point in time are displayed.
    
    > [!div class="mx-imgBorder"]
    > ![View underlying opportunities of a column](media/predictive-forecasting-snapshot-select-column-opportunities.png "View underlying opportunites of a column")

5.	To go back to the forecast, select **Back to forecast**.

### See also

[About premium forecasting](configure-premium-forecasting.md)<br>
[Manage snapshots for a forecast](manage-snapshots-forecast.md)<br>
[Analyze deals flow between snapshots](analyze-deals-flow-between-snapshots.md)