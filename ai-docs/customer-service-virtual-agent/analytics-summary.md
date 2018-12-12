---
title: "Summary dashboard"
description: "Learn about the AI for Customer Service Virtual Agent Summary dashboard."
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

# Summary dashboard

    > [!div class="mx-imgBorder"]
    > ![Summary dashboard](media/dash-summary-1.PNG)

The Summary dashboard gives you a broad overview of your virtual agent's performance and uses artificial intelligence (AI) technology to show you topics that are having the greatest impact on case volume and resolution time.

The Summary dashboard includes a variety of charts with graphical views of your virtual agent's key performance indicators. For information about each chart, click the link for the chart in the following list, or scroll down to the chart's section below.

* [Summary charts](#summary-charts)
* [Engagement rate drivers](#engagement-rate-drivers-chart)
* [Abandon rate drivers](#abandon-rate-drivers-chart)
* [Resolution rate drivers](#resolution-rate-drivers-chart)
* [Customer satisfaction](#customer-satisfaction-chart)
* [Survey response rate](#survey-response-rate-chart)

The Engagement rate drivers, Abandon rate drivers, and Resolution rate drivers charts use natural language understanding artificial intelligence technology to group support cases as topics. These charts show you the topics that are having the most impact on the performance of your virtual agent.

By default, the dashboard shows you key performance indicators for the last seven days. To change the time period to the last 30 days, select **Last 30 days** from the drop-down list at the top of the dashboard.

## Summary charts

    > [!div class="mx-imgBorder"]
    > ![Summary charts](media/analytics-summary-1.PNG)

The summary charts summarize the key performance indicators for the specified time period, and the percent change over the period.

Description | Details
----------- | -------
Total sessions | The total number of sessions within the specified time period.
Engagement rate | The percentage of total sessions that are engaged sessions. An engaged session is a session in which a user-created topic (as opposed to system topic) is triggered, or the session ends in escalation. Engaged sessions can have one of three outcomes -- they are either resolved, escalated, or abandoned.
Resolution rate | The percentage of engaged sessions that are resolved. A resolved session is an engaged session in which the user receives a customer satisfaction (CSAT) survey and either does not respond or responds *Yes*.
Escalation rate | The percentage of engaged sessions that are escalated. An escalated session is an engaged session that is escalated to a human agent.
Abandon rate | The percentage of engaged sessions that are abandoned. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the session.

A blue up and down indicator next to the value indicates the percent change in a positive direction. A red indicator indicates the percent change in a negative direction.

## Escalation rate drivers chart

    > [!div class="mx-imgBorder"]
    > ![Escalation rate drivers chart](media/analytics-summary-2.PNG)

The escalation rate drivers chart uses artificial intelligence technology to group related support cases as topics, and then display topics in order of their impact on the escalation rate over the specified time period.

Description | Details
----------- | -------
Topic | Artificial intelligence clustering of support cases based on language understanding applied to case titles.
Rate | The percentage of engaged sessions for the topic that are escalated. An escalated session is an engaged session that is escalated to a human agent.
Impact | The topic's escalation rate impact score. The escalation rate impact score is the overall escalation rate including the topic minus the overall escalation rate excluding the topic.

The chart displays the impact as a red or blue bar. The midpoint is the overall average escalation rate. A red bar indicates that the topic's escalation rate is larger than the average escalation rate, resulting in a negative impact on overall escalation rate. A blue bar indicates that the resolution time is shorter, resulting in a positive impact on overall escalation rate performance.

Improving the escalation rate for the top escalation rate topics in red will have the greatest impact on improving virtual agent performance.

To see additional information about each topic, click the Detail link to display the Topic details dashboard. For more information, see [Topic details dashboard](analytics-topic-details.md).

## Abandon rate drivers chart

    > [!div class="mx-imgBorder"]
    > ![Abandon rate drivers chart](media/analytics-summary-3.PNG)

The abandon rate drivers chart uses artificial intelligence technology to group related support cases as topics, and then display topics in order of their impact on the abandon rate over the specified time period.

Description | Details
----------- | -------
Topic | Artificial intelligence clustering of cases based on language understanding applied to case titles.
Rate | The percentage of engaged sessions for the topic that are abandoned. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the interaction.
Impact | The topic's abandon rate impact score. The abandon rate impact score is the overall abandon rate including the topic minus the overall abandon rate excluding the topic.

The chart displays the impact as a red or blue bar. The midpoint is the overall average abandon rate. A red bar indicates that the topic's abandon rate is larger than the average abandon rate, resulting in a negative impact on overall abandon rate. A blue bar indicates that the abandon time is shorter, resulting in a positive impact on overall abandon rate performance.

Improving the abandon rate for the top abandon rate topics in red will have the greatest impact on improving virtual agent performance.

To see additional information about each topic, click the Detail link to display the Topic details dashboard. For more information, see [Topic details dashboard](analytics-topic-details.md).

## Resolution rate drivers chart

    > [!div class="mx-imgBorder"]
    > ![Resolution rate drivers chart](media/analytics-summary-4.PNG)

The resolution rate drivers chart uses artificial intelligence technology to group related support cases as topics, and then display topics in order of their impact on the resolution rate over the specified time period.

Description | Details
----------- | -------
Topic | Artificial intelligence clustering of cases based on language understanding applied to case titles.
Rate | The percentage of engaged sessions for the topic that are resolved. A resolved session is an engaged session in which a customer receives an end of session survey and either does not respond to survey or responds *Yes*.
Impact | The topic's resolution rate impact score. The resolution rate impact score is the overall resolution rate including the topic minus the overall resolution rate excluding the topic.

The chart displays the impact as a red or blue bar. The midpoint is the overall average resolution rate. A red bar indicates that the topic's resolution rate is larger than the average resolution rate, resulting in a negative impact on overall resolution rate. A blue bar indicates that the resolution time is shorter, resulting in a positive impact on overall resolution rate performance.

Improving the resolution rate for the top resolution rate topics in red will have the greatest impact on improving virtual agent performance.

To see additional information about each topic, click the Detail link to display the Topic Details dashboard. For more information, see [Topic details dashboard](analytics-topic-details.md).

## Customer satisfaction chart

    > [!div class="mx-imgBorder"]
    > ![Customer satisfaction chart](media/analytics-summary-5.PNG)

The customer satisfaction chart provides a graphical view of the average of customer satisfaction (CSAT) scores for sessions in which customers respond to an end-of-session request to take the survey. The CSAT survey asks customers to rate of their experience on a scale of 1 to 5.

## Survey response rate chart

    > [!div class="mx-imgBorder"]
    > ![Survey response rate chart](media/analytics-summary-6.PNG)

The survey response rate chart provides a graphical view of the rate of response to end-of-session requests to take the CSAT survey.
