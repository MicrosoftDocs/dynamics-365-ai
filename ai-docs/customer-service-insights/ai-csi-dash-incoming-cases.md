---
title: "Incoming Cases dashboard"
description: "Learn about the customer service insights available on the Incoming Cases dashboard."
keywords: ""
ms.date: 9/18/2018
ms.service:
  - "business-applications"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Incoming Cases dashboard​

![Incoming Cases dashboard](media/ai-csi-incoming-cases-dash.png)

The Incoming Cases dashboard gives you an overview of the incoming cases in your customer support system for the specified time period.

You can display [KPI Summary](ai-csi-dash-kpi-summary.md), Incoming Cases, [Case Resolutions](ai-csi-dash-case-resolutions.md), and [Customer Satisfaction](ai-csi-dash-CSAT.md) dashboards by clicking each dashboard's icon in the navigation pane. You can display the [Topic Details](ai-csi-dash-topic-details.md) dashboard by right-clicking a topic in one of the AI Insights charts in those dashboards. The KPI Summary dashboard is the default Dynamics 365 AI for Customer Service dashboard.

The Incoming Cases dashboard provides graphical views of the new support cases, including:

* The daily breakdown between high, medium, and low priority cases.
* The daily breakdown of cases by the support channel customers used; for example, chat window, email, support ticket, Facebook, or Twitter.
* The trends in the timing of cases during the day for each channel during the time period.

In addition, the dashboard uses artificial intelligence technology to show you the new customer support topics that are generating the most case volume, and the topics that are showing the biggest change in volume. This can help you identify emerging issues in your system.

By default, the dashboard shows you key performance indicators for the last week, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month. To display data for a specific product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list.

## Case priority chart

![Case priority chart](media/ai-csi-case-priority-incoming.png)

The case priority chart shows the breakdown in new support cases each day in the specified time period between high, medium, and low priority cases.

## Case channels chart

![Case channels chart](media/ai-csi-case-channels-incoming.png)

The case channels chart shows the breakdown in new support cases each day in the specified time period between different support channels.

## Case timing chart

![Case timing chart](media/ai-csi-case-timing.png)

The case timing chart shows the trends in the time of day of new support cases for each channel during the time period.

## Current popular topics chart (AI Insights)

![Current popular topics chart](media/ai-csi-current-popular-topics.png)

The current popular topics chart uses artificial intelligence technology to group related incoming support cases as support topics, and then display topics in order of volume over the specified time period, showing:

* The percent of the total incoming case volume.
* The number of incoming support cases.
* The average resolution time.
* The resolution rate.
* The average customer satisfaction score for each topic.

To see additional information about each topic, right-click the topic name and select **Drillthrough** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).

## Emerging topics chart (AI Insights)

![Emerging topics chart](media/ai-csi-emerging-topics.png)

The emerging topics chart uses artificial intelligence technology to group related incoming support cases as support topics, and then display the topics in order of the change in volume over the specified time period, showing:

* The percent of the change in volume.
* The number of incoming cases.
* The average resolution time.
* The resolution rate.
* The average customer satisfaction score.

To see additional information about each topic, right-click the topic name and select **Drillthrough** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).