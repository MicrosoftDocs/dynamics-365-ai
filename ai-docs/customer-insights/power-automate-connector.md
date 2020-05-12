---
title: "Power Automate connector | Microsoft Docs"
description: "Create flows in Microsoft Power Automate from Dynamics 365 Customer Insights."
ms.date: 05/12/2020
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
ms.reviewer: philk
manager: shellyha
---

# Power Automate connector (preview)

Trigger specific events to occur automatically when your data changes and manage more complex flows directly in [Power Automate](https://flow.microsoft.com/).

## Power Automate triggers

You can use a variety of triggers that allow you to setup flows to automate daily work tasks, such as notifications or more advanced actions. 

- Trigger when a data source refresh fails 
- Trigger when a data source refresh succeeds
- Trigger when a threshold is crossed on a segment. Note: the trigger is limited to the threshold being surpassed
- Trigger when a threshold is crossed on a business measure. Note: the trigger is limited to the threshold being surpassed

[Configure your triggers in Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).

## Power Automate actions
Our Power Automate connector does provide different actions that can be used next to the available triggers. For more information, see the [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).

## Create a Power Automate flow in Customer Insights

1. In Customer Insights, go to **Admin** > **System**.

1. On the **System** page, select the **Status** tab.

1. In the **Data Sources** section, select **Flows** and select **Create a flow** from the dropdown list.
   > [!div class="mx-imgBorder"]
   > ![Power Automate connector showing Create a Flow action](media/power-automate-connector-create-flow.png "Power Automate connector showing Create a Flow action")

1. In Power Automate, select one of the available triggers to create your preferred flow. If you're creating your first flow, you'll need to authenticate with the Power Automate connector first.
