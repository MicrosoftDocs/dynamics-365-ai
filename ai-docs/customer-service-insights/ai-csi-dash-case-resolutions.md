---
title: "Case resolution dashboard​"
description: "Learn about the customer service insights available on the Case resolution dashboard."
keywords: ""
ms.date: 10/25/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Case resolution dashboard​

> [!div class="mx-imgBorder"]
> ![Case resolution dashboard](media/ai-csi-case-resolutions-dash.png)

The Case resolution dashboard gives you an overview of your customer service system's case resolution performance, including using artificial intelligence (AI) technology to show you topics that are having the greatest positive or negative impact on resolution time.

The Case resolution dashboard includes a variety of charts with graphical views of your system's case resolution data. For information about each chart, click on the link for the chart in the following table, or scroll down to the chart's section below.

Chart | Link
----- | ----
> [!div class="mx-imgBorder"]
> ![Agents with longest resolve time](media/ai-csi-longest-resolve-time.png) | [Agents with longest resolve time](#agents-with-longest-resolve-time-chart)
> [!div class="mx-imgBorder"]
> ![New cases versus average resolve time](media/ai-csi-incoming-vs-resolve-time.png) | [New cases versus average resolve time](#new-cases-versus-average-resolve-time-chart)
> [!div class="mx-imgBorder"]
> ![Agents handling most escalations chart](media/ai-csi-most-escalations.png) | [Agents handling most escalations](#agents-handling-most-escalations-chart)
> [!div class="mx-imgBorder"]
> ![New escalations versus resolved escalations chart](media/ai-csi-new-resolved-escalations.png) | [New escalations versus resolved escalations](#new-escalations-versus-resolved-escalations-chart)
> [!div class="mx-imgBorder"]
> ![Top resolution time impactors](media/ai-csi-resolution-time-impactors.png) | [Top resolution time impactors (AI Insights)](#top-resolution-time-impactors-chart)

The *Top resolution time impactors* chart uses natural language understanding artificial intelligence technology to group support cases as *topics* that are a collection of related cases. This chart shows you the customer support topics that are having the most impact on case resolution time, helping you identify areas for improvement that can have the greatest impact on system performance.

By default, the dashboard shows you key performance indicators for the last month, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month.

To filter data by product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list. For more information on working with filters, see [Work with dashboards and sample data](ai-csi-use-dash-sample-data.md).

## Agents with longest resolve time chart

> [!div class="mx-imgBorder"]
> ![Agents with longest resolve time chart](media/ai-csi-longest-resolve-time.png)

The agents with longest resolve time chart shows the average time, in minutes, that it takes each agent in the specified time period to resolve a customer support case, in reverse order of resolution time, and the breakdown by priority.

Description | Details
----------- | -------
Agents with longest resolve time | *Resolved case resolution time breakdown by agent and case priority*

## New cases versus average resolve time chart

> [!div class="mx-imgBorder"]
> ![Incoming cases versus average resolve time chart](media/ai-csi-incoming-vs-resolve-time.png)

The incoming cases versus average resolve time chart shows the daily trend in the specified time period in the number of incoming support cases and the average resolution time, in minutes.

Description | Details
----------- | -------
Incoming cases | *Daily number of incoming cases*
Average resolution time | *Daily average case resolution time*

## Agents handling most escalations chart

> [!div class="mx-imgBorder"]
> ![Agents handling most escalations chart](media/ai-csi-most-escalations.png)

The agents handling most escalations chart shows the number of active and resolved support cases for each agent, in order of total cases.

Description | Details
----------- | -------
Agents handling most escalations | *Number of active and resolved cases by agent*

## New escalations versus resolved escalations chart

> [!div class="mx-imgBorder"]
> ![New escalations versus resolved escalations chart](media/ai-csi-new-resolved-escalations.png)

The new escalations versus resolved escalations chart shows the daily trend in the number of new support cases that are escalated and the number of escalated cases that are resolved.

Description | Details
----------- | -------
New escalations | *Daily number of escalated cases*
Resolved escalations | *Daily number of escalated cases that are resolved*

## Top resolution time impactors chart

> [!div class="mx-imgBorder"]
> ![Top resolution time impactors](media/ai-csi-resolution-time-impactors.png)

The top resolution time impactors chart uses artificial intelligence technology to group related support cases as support topics, and then display topics in order of resolution time over the specified time period.

Description | Details
----------- | -------
Topic | *Artificial intelligence clustering of cases based on language understanding applied to case titles*
Volume | *The total resolved cases associated with this topic divided by total resolved cases*
Average resolve time | *The average resolution time of resolved cases within the specified time period*
Impact | 1 – (*Average resolution time not including the current topic divided by overall average resolution time for all topics*)

The chart displays the impact as a red or blue bar. The midpoint is the overall average case resolution time. A red bar indicates that the topic's resolution time is longer than the average case resolution time, resulting in a negative impact on overall case resolution performance. A blue bar indicates that the resolution time is shorter, resulting in a positive impact on overall case resolution performance. Improving case resolution time for the top resolve time topics in red will have the greatest impact on improving overall system performance.

To see additional information about each topic, right-click the topic name, hover over **Drillthrough**, and then select **Topic Drill Through** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-dash-topic-details.md).
