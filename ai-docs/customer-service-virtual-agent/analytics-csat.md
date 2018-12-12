---
title: "Customer satisfaction rate dashboard"
description: "Learn about the AI for Customer Service Virtual Agent Customer satisfaction dashboard."
keywords: ""
ms\.date: 12/5/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Customer satisfaction dashboard

> [!div class="mx-imgBorder"]
> ![Customer satisfaction dashboard](media/dash-csat-1.PNG)

The Customer satisfaction dashboard provides a detailed view of customer satisfaction (CSAT) survey data, including average CSAT score over time and the topics that and having the most impact on the CSAT score. 

The Customer satisfaction dashboard includes a variety of charts with graphical views of your virtual agent's customer satisfaction indicators. For information about each chart, click the link for the chart in the following list, or scroll down to the chart's section below.

* [Customer satisfaction drivers chart](#customer-satisfaction-drivers-chart)
* [CSAT summary charts](#csat-summary-charts)
* [Scores over time chart](#scores-over-time-chart)
* [Score breakdown chart](#score-breakdown-chart)

The Customer satisfaction drivers chart uses natural language understanding artificial intelligence technology to group support cases as topics. This chart shows you the topics that are having the most impact on customer satisfaction.

By default, the dashboard shows you key performance indicators for the last seven days. To change the time period to the last 30 days, select **Last 30 days** from the drop-down list at the top of the dashboard.

## Customer satisfaction drivers chart

> [!div class="mx-imgBorder"]
> ![Customer satisfaction drivers chart](media/analytics-csat-1.PNG)

The Customer satisfaction drivers chart uses artificial intelligence technology to group related support cases as topics, and then display topics in order of their impact on customer satisfaction over the specified time period.

Description | Details
----------- | -------
Topic | Artificial intelligence clustering of support cases based on language understanding applied to case titles.
Total sessions | The total number of sessions for the topic within the specified time period.
Resolution rate | The percentage of engaged sessions for the topic that are resolved. A resolved session is an engaged session in which the user receives a customer satisfaction (CSAT) survey and either does not respond or responds *Yes*.
Abandon rate | The percentage of engaged sessions for the topic that are abandoned. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the session.
Escalation rate | The percentage of engaged sessions for the topic that are escalated. An escalated session is an engaged session that is escalated to a human agent.
Avg CSAT | The average CSAT survey score for the topic.
Impact | The topic's customer satisfaction impact score. The customer satisfaction impact score is the overall average CSAT survey score including the topic minus the overall average CSAT survey score excluding the topic.

The chart displays the impact as a red or blue bar. The midpoint is the overall average CSAT survey score. A red bar indicates that the topic's average CSAT survey score is lower than the average average CSAT survey score, resulting in a negative impact on overall average CSAT survey score. A blue bar indicates that the average CSAT survey score is higher, resulting in a positive impact on overall average CSAT survey score.

Improving the average CSAT survey score for the top customer satisfaction impact topics in red will have the greatest impact on improving customer satisfaction.

To see additional information about each topic, click the Detail link to display the Topic details dashboard. For more information, see [Topic details dashboard](analytics-topic-details.md).

## CSAT summary charts

> [!div class="mx-imgBorder"]
> ![CSAT summary charts](media/analytics-csat-2.PNG)

The CSAT summary charts summarize the key customer satisfaction performance indicators for the specified time period, and the percent change over the period.

Description | Details
----------- | -------
Customer satisfaction | The average CSAT survey score for the specified time period.
Survey response rate | The percentage of sessions in which a customer responded to a CSAT survey request during the specified time period.
Surveys completed | The number of CSAT surveys completed during the specified time period.

A blue up and down indicator below the value indicates the percent change in a positive direction. A red indicator indicates the percent change in a negative direction.

## Scores over time chart

> [!div class="mx-imgBorder"]
> ![Scores over time chart](media/analytics-csat-3.PNG)

The scores over time chart provides a graphical view of the average CSAT score over the specified time period.

## Score breakdown chart

> [!div class="mx-imgBorder"]
> ![Score breakdown chart](media/analytics-csat-4.PNG)

The score breakdown chart provides a graphical view of the breakdown in CSAT score by average score and whether the survey indicated one of the following:

* The solution didn't align with the query.
* The customer tried the solution but it didn't work.
* The virtual agent didn't understand the customer's query.