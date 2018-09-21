---
title: "KPI Summary dashboard"
description: "Learn about the customer service insights available on the KPI Summary dashboard​."
keywords: ""
ms.date: 9/11/2018
ms.service:
  - "business-applications"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# KPI Summary dashboard

![KPI Summary dashboard](media/ai-customer-service-insights.png)

The KPI (Key Performance Indicator) Summary dashboard gives you a broad overview of the performance of your customer support system. The dashboard shows you key performance indicators such as the number of incoming, resolved, escalated, and SLA compliant cases for a specified time period, and the average resolution time and customer satisfaction score.

The dashboard also provides a variety of graphical views of your system's support cases, including:

* The breakdown of case priority, backlog and new cases, and case channels.
* The aggregate trend in new and resolved cases.
* The breakdown of unresolved cases by age.

In addition, the dashboard uses artificial intelligence technology to show you the customer support topics that are generating the most volume, and the topics that are having the most impact on case resolution time. This can help you identify areas for improvement that can have the greatest impact on improving overall system performance.

By default, the dashboard shows you key performance indicators for the last week, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month. To display data for a specific product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list.

## Key performance indicator charts

![Key performance indicator charts](media/ai-csi-kpi-charts.png)

The key performance indicator charts display a variety of key support system data for the specified time period, and the percent change over the period:

* The number of new (incoming) support cases.
* The number of resolved support cases.
* The number of escalated support cases.
* The number of support cases that are compliant with their service level agreement (SLA).
* The average case resolution time.
* The average customer satisfaction score (CSAT).

## Case priority chart

![Case priority chart](media/ai-csi-case-priority.png)

The case priority chart shows the percentage breakdown for the specified time period between high, normal, and low priority support cases.

## Total case breakdown chart

![Total case breakdown chart](media/ai-csi-total-case-breakdown.png)

The total case breakdown chart shows the breakdown in support cases for the specified time period between new cases and backlog cases that were carried over from earlier. Backlog cases are support cases that were unresolved at the beginning of the specified time period.

## Case channels chart

![Case channels chart](media/ai-csi-case-channels.png)

The case channels chart shows the breakdown in support cases for the specified time period by support channel.

## Case tracking chart

![Case tracking chart](media/ai-csi-case-tracking.png)

The case tracking chart shows the trend in the number of incoming support cases for the specified time period as well as the trend in how many cases are being resolved.

## Unresolved cases by age chart

![Unresolved cases by age chart](media/ai-csi-cases-by-age.png)

The unresolved cases by age chart shows the relative number of support cases for the specified time period by how many days ago they were created.

## Top case volume impactors chart

![Top case volume impactors chart](media/ai-csi-top-case-volume.png)

The top case volume impactors chart uses artificial intelligence technology to group related customer support cases as support *topics*, and then display the topics in order of volume over the specified time period, showing both the percent of total volume and number of cases for each topic.

To see additional information about each topic, right-click the topic name and select **Drillthrough** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).

## Top resolve time impactors chart

![Top resolve time impactors chart](media/ai-csi-top-resolve-time.png)

The top case volume impactors chart displays support topics in order of resolution time over the specified time period, showing the average resolution time for each topic's support cases and the impact that resolution time is having on system performance.

The chart displays the impact as a red or blue bar. The midpoint is the overall average case resolution time. A red bar indicates that the topic's resolution time is longer than the average case resolution time. A blue bar indicates that the resolution time is shorter. Improving case resolution time for the top resolve time topics in red will have the greatest impact on improving overall system performance.

To see additional information about each topic, right-click the topic name and select **Drillthrough** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).
