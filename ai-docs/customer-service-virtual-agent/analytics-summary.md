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

The Summary dashboard gives you a broad overview of the customer service experience at your organization, including using artificial intelligence (AI) technology to show you topics that are having the greatest impact on case volume and resolution time.

The Summary dashboard includes a variety of charts with graphical views of your system's key performance indicators. For information about each chart, click the link for the chart in the following list, or scroll down to the chart's section below.

* [Summary charts](#summary-charts)
* [Engagement rate drivers](#engagement-rate-drivers-chart)
* [Abandon rate drivers](#abandon-rate-drivers-chart)
* [Customer satisfaction](#customer-satisfaction-chart)
* [Resolution rate drivers](#resolution-rate-drivers-chart)
* [Survey response rate](#survey-response-rate-chart)

The *Engagement rate drivers*, *Abandon rate drivers*, and *Resolution rate drivers* charts use natural language understanding artificial intelligence technology to group support cases as topics. These charts show you the topics that are having the most impact on your customer support system. You can then use the Virtual Agent Designer to create a virtual agent for those topics.

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
Topic | Artificial intelligence clustering of cases based on language understanding applied to case titles.
Rate | The percentage of engaged sessions for the topic that are escalated. An escalated session is an engaged session that is escalated to a human agent.
Impact | The topic's escalation rate impact score. The escalation rate impact score is the overall escalation rate including the topic minus the overall escalation rate excluding the topic.

The chart displays the impact as a red or blue bar. The midpoint is the overall average escalation rate. A red bar indicates that the topic's escalation rate is larger than the average escalation rate, resulting in a negative impact on overall escalation rate. A blue bar indicates that the resolution time is shorter, resulting in a positive impact on overall escalation rate performance.

Improving the escalation rate for the top escalation rate topics in red will have the greatest impact on improving overall system performance. To help you improve the escalation rate, you can create a virtual agent for the topic in the Virtual Agent Designer.

To see additional information about each topic, click the Detail link to display the Topic Details dashboard. For more information, see [Topic details dashboard](analytics-topic-details.md).

## Abandon rate drivers chart

## Resolution rate drivers chart

## Customer satisfaction chart

## Survey response rate chart
