---
title: "Resolution dashboard​"
description: "Learn about the customer service insights available on the Resolution dashboard."
keywords: ""
ms\.date: 1/23/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Resolutions dashboard​

[!INCLUDE [public-preview](../includes/public-preview.md)]

> [!div class="mx-imgBorder"]
> ![Resolutions dashboard](media/ai-csi-resolutions-dash.png)

The Resolutions dashboard gives you an overview of your customer service system's case resolution performance. It uses artificial intelligence (AI) technology to show you topics that are having the greatest positive or negative impact on resolution time.

The Resolutions dashboard includes a variety of charts with graphical views of your system's case resolution data. For information about each chart, click the link for the chart in the following list or scroll to locate the chart later in this topic.

* [Agents with longest resolve time](#agents-with-longest-resolve-time-chart)
* [New cases versus average resolution time](#new-cases-versus-average-resolution-time-chart)
* [Agents handling most escalations](#agents-handling-most-escalations-chart)
* [New escalations versus resolved escalations](#new-escalations-versus-resolved-escalations-chart)
* [Resolution time drivers (AI Insights)](#resolution-time-drivers-chart)

The Resolution time drivers chart uses natural language understanding to group support cases as *topics* that are a collection of related cases. This chart shows you the customer support topics that are having the most impact on case resolution time, helping you identify areas for improvement that can have the greatest impact on system performance.

By default, the dashboard shows you key performance indicators for the last month, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the **Time period** drop-down list at the top of the dashboard. You can select either last day, last week, or last month.

To filter data by product, channel, business unit, or team, select a value from the **Product**, **Channel**, **Business Unit**, or **Team** drop-down list. If you switch to a different dashboard, the filter you specify persists and is applied to the data on all dashboards. For more information on working with filters, see [Work with Customer Service Insights dashboards](use-dashboard-sample-data.md).

## Agents with longest resolve time chart

> [!div class="mx-imgBorder"]
> ![Agents with longest resolve time chart](media/ai-csi-longest-resolve-time.png)

The Agents with longest resolve time chart shows the average time, in minutes, that it takes each agent in the specified time period to resolve a customer-support case, in reverse order of resolution time.

Description | Details
----------- | -------
Agents with longest resolve time | Resolved case resolution time breakdown by agent

## New cases versus average resolution time chart

> [!div class="mx-imgBorder"]
> ![New cases versus average resolution time chart](media/ai-csi-incoming-vs-resolution-time.png)

The New cases versus average resolution time chart shows the daily trend in the specified time period in the number of new support cases and the average resolution time, in minutes.

Description | Details
----------- | -------
Incoming cases | Daily number of incoming cases
Average resolution time | Daily average case resolution time

## Agents handling most escalations chart

> [!div class="mx-imgBorder"]
> ![Agents handling most escalations chart](media/ai-csi-most-escalations.png)

The Agents handling most escalations chart shows the number of active and resolved support cases for each agent, in order of total cases.

Description | Details
----------- | -------
Agents handling most escalations | Number of active and resolved cases by agent

## New escalations versus resolved escalations chart

> [!div class="mx-imgBorder"]
> ![New escalations versus resolved escalations chart](media/ai-csi-new-resolved-escalations.png)

The New escalations versus resolved escalations chart shows the daily trend in the number of new support cases that are escalated and the number of escalated cases that are resolved.

Description | Details
----------- | -------
New escalations | Daily number of escalated cases
Resolved escalations | Daily number of escalated cases that are resolved

## Resolution time drivers chart

> [!div class="mx-imgBorder"]
> ![Resolution time drivers](media/ai-csi-resolution-drivers.png)

The Resolution time drivers chart uses artificial intelligence technology to group related support cases as support topics and then display topics in order of resolution time over the specified time period.

Description | Details
----------- | -------
Topic | Artificial intelligence clustering of cases based on language understanding applied to case titles
Volume | The total resolved cases associated with this topic divided by total resolved cases
Average resolution time | The average resolution time of resolved cases within the specified time period
Impact | 1 – (Average resolution time not including the current topic divided by overall average resolution time for all topics)

The chart displays the impact as a red or blue bar. The midpoint is the overall average case resolution time. A red bar indicates that the topic's resolution time is longer than the average case resolution time, resulting in a negative impact on overall case resolution performance. A blue bar indicates that the resolution time is shorter, resulting in a positive impact on overall case resolution performance. Improving case-resolution time for the top resolve-time topics in red will have the greatest impact on improving overall system performance.

To see additional information about each topic, right-click the topic name, hover over **Drillthrough**, and then select **Topic drillthrough** to display the Topic details dashboard. For more information, see [Topic details dashboard](dashboard-topic-details.md).
