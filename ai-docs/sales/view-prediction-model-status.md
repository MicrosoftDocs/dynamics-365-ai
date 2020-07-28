---
title: "View and understand the status of prediction column in a forecast | MicrosoftDocs"
description: "View and understand the status of prediction column in a forecast."
ms.date: 08/01/2020
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# View prediction model status 

<!--Early access preview note will be added here-->

You can view the details of the prediction model, such as last calculated date and errors in a forecast. After a calculation or recalculation, an icon is displayed corresponding to **Prediction** column in the [Layout configuration step](https://docs.microsoft.com/dynamics365/sales-enterprise/choose-layout-and-columns-forecast) of a forecast. Based on the icon you can determine whether the model is successful or not.

>[!NOTE]
>After you configure and publish a forecast for the first time with prediction column, the column takes about two hours to display the data. 

## On successful calculation

Upon a successful calculation or recalculation, an information icon is displayed corresponding the **Prediction** column. Select the information icon and a side pane is displayed with information about when the prediction model is last calculated.

> [!div class="mx-imgBorder"]
> ![Successful calculation of prediction model](media/predictive-forecasting-successful-model-creation.png "Successful calculation of prediction model")

## On erroneous calculation

When the calculation or recalculation fails, an alert icon is displayed corresponding the **Prediction** column. Select the alert icon and a side pane is displayed with information on errors or warnings specifying why the calculation of the model failed. Depending on these errors and warnings, you can take necessary steps to resolve the issues to recalculate the model.

> [!div class="mx-imgBorder"]
> ![Erroneous calculation of prediction model](media/predictive-forecasting-erroneous-model-creation.png "Erroneous calculation of prediction model")

## See also

[Premium forecasting](configure-premium-forecasting.md)