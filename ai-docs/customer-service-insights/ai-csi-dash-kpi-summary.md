---
title: "KPI summary dashboard"
description: "Learn about the customer service insights available on the KPI Summary dashboard​."
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

# KPI summary dashboard

![KPI summary dashboard](media/ai-csi-kpi-summary-dash.png)

The KPI (Key Performance Indicator) summary dashboard gives you a broad overview of your customer service experience, including using artificial intelligence (AI) technology to show you topics that are having the greatest impact on volume and resolution time.

The KPI summary dashboard includes a variety of charts with graphical views of your system's key performance indicators. For information about each chart, click on the link for the chart in the following table, or scroll down to the chart's section below.

Chart | Link
----- | ----
![KPI summary charts](media/ai-csi-kpi-charts.png) | [KPI summary charts](#kpi-summary-charts)
![Total case breakdown](media/ai-csi-total-case-breakdown.png) | [Total case breakdown](#total-case-breakdown-chart)
![Case priority](media/ai-csi-case-priority.png) | [Case priority](#case-priority-chart)
![Case channel](media/ai-csi-case-channels.png) | [Case channel](#case-channel-chart)
![Case tracking](media/ai-csi-case-tracking.png) | [Case tracking](#case-tracking-chart)
![Unresolved cases by age](media/ai-csi-cases-by-age.png) | [Unresolved cases by age](#unresolved-cases-by-age-chart)
![Top case volume impactors](media/ai-csi-top-case-volume.png) | [Top case volume impactors (AI Insights)](#top-case-volume-impactors-chart)
![Emerging topics](media/ai-csi-top-resolve-time.png) | [Emerging topics (AI Insights)](#emerging-topics-chart)

The *Top case volume impactors* and *Top resolve time impactors* charts use natural language understanding artificial intelligence technology to group support cases as *topics* that are a collection of related cases. These charts show you the customer support topics that are generating the most volume and the topics that are having the most impact on case resolution time, helping you identify areas for improvement that can have the greatest impact on system performance.

By default, the dashboard shows you key performance indicators for the last month, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month.

To filter data by product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list. For more information on working with filters, see [Work with dashboards and sample data](ai-csi-use-dash-sample-data.md).

## KPI summary charts

![KPI summary charts](media/ai-csi-kpi-charts.png)

The KPI summary charts summarize the key performance indicators for the specified time period, and the percent change over the period:

Description | Details
----------- | -------
Total cases | *New cases created within the specified time period* + *Rollover cases (including all rollover cases that are active, resolved or cancelled within the specified time period)*
Resolutions | *All cases resolved within specified time period*
Escalations | *All cases escalated within specified time period*
SLA compliant | *Of the total cases, the cases that are SLA compliant* (including rollover cases and new cases that are SLA compliant)
Average resolution time | *The average resolution time of all cases resolved within specified time period*
Average CSAT | *The sum of CSAT scores* / *The count of resolved cases that have CSAT values*

A blue up and down indicator next the value indicates the percent change in a positive direction. A red indicator indicates the percent change in a negative direction.

## Case priority chart

![Case priority chart](media/ai-csi-case-priority.png)

The case priority chart shows the percentage breakdown for the specified time period between high, normal, and low priority support cases.

Description | Details
----------- | -------
Case priority | *Total case breakdown by case priority*

## Total case breakdown chart

![Total case breakdown chart](media/ai-csi-total-case-breakdown.png)

The total case breakdown chart shows the breakdown in support cases for the specified time period between new cases and backlog cases that were carried over from earlier. Backlog cases are support cases that were unresolved at the beginning of the specified time period.

Description | Details
----------- | -------
Total case breakdown | *Total case breakdown by rollover cases (backlog) plus new cases for the specified time period*

## Case channel chart

![Case channel chart](media/ai-csi-case-channels.png)

The case channel chart shows the breakdown in support cases for the specified time period by support channel.

Description | Details
----------- | -------
Case channels | *Total case breakdown by channel*

## Case tracking chart

![Case tracking chart](media/ai-csi-case-tracking.png)

The case tracking chart shows the trend in the number of new support cases for the specified time period as well as the trend in how many cases are being resolved.

Description | Details
----------- | -------
New | *The number of cases created each day for the specified time period*
Resolved | *The number of cases resolved each day for the specified time period*

## Unresolved cases by age chart

![Unresolved cases by age chart](media/ai-csi-cases-by-age.png)

The unresolved cases by age chart shows the relative number of support cases for the specified time period by how many days ago they were created.

Description | Details
----------- | -------
Unresolved cases by age | *Total unresolved cases by days unresolved*

## Top case volume impactors chart

![Top case volume impactors chart](media/ai-csi-top-case-volume.png)

The top case volume impactors chart uses artificial intelligence technology to group related support cases as support topics, and then display topics in order of volume over the specified time period, showing both the percent of total volume and number of cases for each topic.

Description | Details
----------- | -------
Topic | *Artificial intelligence clustering of cases based on language understanding applied to case titles*
Volume | *The total cases associated with this topic divided by total cases*
Total cases | *The total cases associated with this topic*

To see additional information about each topic, right-click the topic name, hover over **Drillthrough**, and then select **Topic Drill Through** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).

## Emerging topics chart

![Emerging topics chart](media/ai-csi-top-resolve-time.png)

The emerging topics chart displays support topics that have a high volume change in order of volume over the specified time period.

Description | Details
----------- | -------
Topic | *Artificial intelligence clustering of cases based on language understanding applied to case titles*
Volume change | *The percent change in volume over the specified time period*
Total cases | *The total cases associated with this topic*

To see additional information about each topic, right-click the topic name, hover over **Drillthrough**, and then select **Topic Drill Through** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).
