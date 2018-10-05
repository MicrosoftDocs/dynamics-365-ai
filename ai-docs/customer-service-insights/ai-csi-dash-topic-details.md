---
title: "Topic Details dashboard"
description: "Learn about the customer service insights available on the Topic Details dashboard​."
keywords: ""
ms.date: 10/5/2018
ms.service:
  - "business-applications"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Topic Details dashboard

![Topic Details dashboard](media/ai-csi-topic-details-dash.png)

The Topic Details dashboard gives you a detailed overview of key performance indicators for a specific topic, including using natural language understanding (AI) technology to show you the impact by product and channel on customer satisfaction scores and resolution time for the topic.

The Topic Details dashboard is not available on the dashboard navigation pane. You can display the dashboard by right-clicking a topic in one of the AI Insights charts on the [KPI Summary](ai-csi-dash-kpi-summary.md), [Incoming Cases](ai-csi-dash-incoming-cases.md), [Case Resolutions](ai-csi-dash-case-resolutions.md), or [Customer Satisfaction](ai-csi-dash-CSAT.md) dashboard. Hover over **Drillthrough** and then click **Topic Drill Through** to display the dashboard.

![Topic Details Drillthrough](media/ai-csi-topic-details-drillthrough.png)

The Topic Details dashboard includes a variety of charts with graphical views of key performance indicators for the topic. For information about each chart, click on the link for the chart in the following table, or scroll down to the chart's section below.

Chart | Link
----- | ----
![Topic Details KPI charts](media/ai-csi-topic-details-kpi-charts.png) | [Topic Details KPI charts](#topic-details-kpi-charts)
![Overall impact charts](media/ai-csi-overall-impact.png) | [Overall impact charts](#overall-impact-charts)
![Agents with most unresolved cases chart](media/ai-csi-agents-unresolved.png) | [Agents with most unresolved cases](#agents-with-most-unresolved-cases-chart)
![Agents with longest resolve time chart](media/ai-csi-agents-resolve-time.png) | [Agents with longest resolve time](#agents-with-longest-resolve-time-chart)
![Agents with lowest CSAT chart](media/ai-csi-lowest-CSAT.png) | [Agents with lowest CSAT](#agents-with-lowest-csat-chart)
![Topic journey chart](media/ai-csi-topic-journey.png) | [Topic journey](#topic-journey-chart)
![Top CSAT impactors chart](media/ai-csi-top-CSAT-impactors.png) | [Top CSAT impactors (AI Insights)](#top-csat-impactors-chart)
![Top resolve time impactors chart](media/ai-csi-top-resolve-time-impactors.png) | [Top resolve time impactors (AI Insights)](#top-resolve-time-impactors-chart)

The *Top CSAT impactors* and *Top resolve time impactors* charts use artificial intelligence technology to group support cases as *topics* that are a collection of related cases. These charts show you the impact the topic's cases have had on customer satisfaction and resolution time, and the channels associated with the topic that are having the greatest impact on customer satisfaction and resolution time. This can help you identify areas for improvement that can have the greatest impact.

By default, the dashboard shows you key performance indicators for the last week, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month.

To filter data by product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list. For more information on working with filters, see [Work with dashboards and sample data](ai-csi-use-dash-sample-data.md).

## Topic Details KPI charts

![Topic Details KPI charts](media/ai-csi-topic-details-kpi-charts.png)

The topic details KPI charts display a variety of key performance indicators for the topic's support cases during the specified time period:

* The number of new (incoming) support cases.
* The number of resolved support cases.
* The number of escalated support cases.
* The number of support cases that are compliant with their service level agreement (SLA).
* The average case resolution time.
* The average customer satisfaction score (CSAT).

## Overall impact charts

![Overall impact charts](media/ai-csi-overall-impact.png)

The overall impact charts show:

* The percent difference between the average customer satisfaction score for the topic's support cases during the specified time period and the overall average customer satisfaction score during the period.
* The percent difference between the average resolution time for the topic's support cases during the specified time period and the overall average resolution time during the period.

## Agents with most unresolved cases chart

![Agents with most unresolved cases chart](media/ai-csi-agents-unresolved.png)

The agents with most unresolved cases chart shows the number of unresolved support cases for each agent for the topic in the specified time period.

## Agents with longest resolve time chart

![Agents with longest resolve time chart](media/ai-csi-agents-resolve-time.png)

The agents with longest resolve time chart shows the average resolution time for each agent for the topic's support cases in the specified time period.

## Agents with lowest CSAT chart

![Agents with lowest CSAT chart](media/ai-csi-lowest-CSAT.png)

The agents with lowest CSAT chart shows the average customer satisfaction score for each agent for the topic's support cases in the specified time period.

## Topic journey chart

![Topic journey chart](media/ai-csi-topic-journey.png)

The topic journey chart shows the path of the topic's support cases during the specified time period from the support channel where they were opened, and whether they were escalated, to their status at the end of the specified time period.

## Top CSAT impactors chart (AI Insights)

![Top CSAT impactors chart](media/ai-csi-top-CSAT-impactors.png)

The top CSAT impactors chart uses artificial intelligence technology to show the top customer satisfaction impactors for the topic during the specified time period by support channel and product. The chart includes:

* The support channel and product.
* The average resolution time for the channel and product's support cases.
* The average customer satisfaction score for the channel and product's support cases.
* The impact that the channel and product are having on the overall customer satisfaction score.

The chart displays the impact as a red or blue bar. The midpoint is the overall average customer satisfaction score (CSAT). A red bar indicates that the CSAT score is lower than the average CSAT score. A blue bar indicates that the CSAT score is higher. Improving customer satisfaction for the top CSAT impactors topics in red will have the greatest impact on improving overall customer satisfaction.

## Top resolve time impactors chart (AI Insights)

![Top resolve time impactors chart](media/ai-csi-top-resolve-time-impactors.png)

The top resolve time impactors chart uses artificial intelligence technology to show the top resolution time impactors for the topic during the specified time period by support channel and product. The chart includes:

* The support channel and product.
* The average resolution time for the channel and product's support cases.
* The average customer satisfaction score for the channel and product's support cases.
* The impact that the channel and product are having on the overall resolution time.

The chart displays the impact as a red or blue bar. The midpoint is the overall average case resolution time. A red bar indicates that the topic's resolution time is longer than the average case resolution time. A blue bar indicates that the resolution time is shorter. Improving case resolution time for the top resolve time impactor topics in red will have the greatest impact on improving overall resolution time.