---
title: "Customer satisfaction rate dashboard"
description: "Learn about the Dynamics 365 Customer Service Virtual Agent Customer satisfaction dashboard."
keywords: ""
ms\.date: 1/14/2019
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

The Customer satisfaction dashboard provides a detailed view of customer satisfaction (CSAT) survey data, including the average CSAT score over time and the topics that are having the most impact on the CSAT score.

The Customer satisfaction dashboard includes a variety of charts with graphical views of your virtual agent's customer satisfaction indicators. For information about each chart, select the link for the chart in the following list, or scroll to find the section about the chart later in this topic:

<!--note from editor: "Score breakdown chart" is a bullet item but section missing. "Scores over time" chart missing some content?-->

* [Customer satisfaction drivers chart](#customer-satisfaction-drivers-chart)
* [CSAT summary charts](#csat-summary-charts)
* [Scores over time chart](#scores-over-time-chart)
* [Score breakdown chart](#score-breakdown-chart)

The Customer satisfaction drivers chart shows you the topics that are having the most impact on customer satisfaction.

By default, the dashboard shows you key performance indicators for the last seven days. To change the time period to the last 30 days, select **Last 30 days** from the drop-down list at the top of the dashboard.

## Customer satisfaction drivers chart

   > [!div class="mx-imgBorder"]
   > ![Customer satisfaction drivers chart](media/analytics-csat-1.PNG)

The Customer satisfaction drivers chart uses artificial intelligence technology to group related support cases as topics. This chart then displays topics in order of their impact on customer satisfaction over the specified time period.

Description | Details
----------- | -------
Topic | A Virtual Agent Designer topic.
Engaged sessions | The number of engaged sessions for the topic within the specified time period.
Resolution rate | The percentage of engaged sessions for the topic that are resolved. A resolved session is an engaged session in which the user receives a customer satisfaction (CSAT) survey and either does not respond or responds *Yes*.
Abandon rate | The percentage of engaged sessions for the topic that are abandoned. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the session.
Escalation rate | The percentage of engaged sessions for the topic that are escalated. An escalated session is an engaged session that is escalated to a human agent.
Avg CSAT | The average CSAT survey score for the topic.
Impact | The topic's customer-satisfaction impact score. The customer-satisfaction impact score is the overall average CSAT survey score including the topic minus the overall average CSAT survey score excluding the topic.

The chart displays the impact as a red or blue bar. A red bar indicates that the topic's average CSAT survey score is lower than the average CSAT survey score, resulting in a negative impact on the overall average CSAT survey score. A blue bar indicates that the average CSAT survey score is higher, resulting in a positive impact on the overall average CSAT survey score.

Improving the average CSAT survey score for the top customer-satisfaction impact topics in red has the greatest impact on improving the overall CSAT score.

To see additional information about each topic, select the Detail link to display the Topic details dashboard. For more information, see [Topic details dashboard](analytics-topic-details.md).

## CSAT summary charts

   > [!div class="mx-imgBorder"]
   > ![CSAT summary charts](media/analytics-csat-2.PNG)

The CSAT summary charts summarize the key customer-satisfaction performance indicators for the specified time period and the percent change over the period.

Description | Details
----------- | -------
Average CSAT score | The average CSAT survey score for the specified time period.
Survey response rate | The percentage of sessions in which a customer responded to a CSAT survey request during the specified time period.
Surveys completed | The number of CSAT surveys completed during the specified time period.

A blue up-and-down indicator below the value indicates the percent change in a positive direction. A red indicator indicates the percent change in a negative direction.

## Scores over time chart

   > [!div class="mx-imgBorder"]
   > ![Scores over time chart](media/analytics-csat-3.PNG)

The Scores over time chart provides a graphical view of the average CSAT score over the specified time period.
