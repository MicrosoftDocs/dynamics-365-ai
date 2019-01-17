---
title: "Topic details dashboard"
description: "Learn about the Dynamics 365 Customer Service Virtual Agent Topic details dashboard."
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

# Topic details dashboard

   > [!div class="mx-imgBorder"]
   > ![Topic details dashboard](media/analytics-topic-details-1.PNG)

The Topic details dashboard provides a view into the performance of individual topics and how they can be improved.

You can display the Topic details dashboard by selecting the Detail link in one of the following charts on the [Summary](analytics-summary.md) and [Customer satisfaction](analytics-CSAT.md) dashboards:

* [Escalation rate drivers (Summary dashboard)](analytics-summary.md#escalation-rate-drivers-chart)
* [Abandon rate drivers (Summary dashboard)](analytics-summary.md#abandon-rate-drivers-chart)
* [Resolution rate drivers (Summary dashboard)](analytics-summary.md#resolution-rate-drivers-chart)
* [Customer satisfaction drivers chart (Customer satisfaction dashboard)](analytics-CSAT.md#customer-satisfaction-drivers-chart)

   > [!div class="mx-imgBorder"]
   > ![Topic details link](media/analytics-overview-1.PNG)

The Topic details dashboard includes a variety of charts with graphical views of a topic's key performance indicators. For information about each chart, select the link for the chart in the following list, or scroll to find the section about the chart later in this topic:

* [Topic summary charts](#topic-summary-charts)
* [Impact summary charts](#impact-summary-charts)
* [Topic volume by day chart](#topic-volume-by-day-chart)

## Topic summary charts

   > [!div class="mx-imgBorder"]
   > ![Topic summary charts](media/analytics-topic-details-2.PNG)

The Topic summary charts summarize the topic's performance indicators for the specified time period and the percent change over the period.

<!--note from editor: Line 50: "An engaged session is either a session in which a user-created topic (as opposed to a system topic) is triggered or a session that continues as an escalation" ?-->

Description | Details
----------- | -------
Total sessions | The total number of sessions within the specified time period.
Engagement rate | The percentage of total sessions that are engaged sessions. An engaged session is a session in which a user-created topic (as opposed to system topic) is triggered, or the session ends in escalation. Engaged sessions can have one of three outcomes--they are either resolved, escalated, or abandoned.
Resolution rate | The percentage of engaged sessions that are resolved. A resolved session is an engaged session in which the user receives a customer satisfaction (CSAT) survey and either does not respond or responds *Yes*.
Escalation rate | The percentage of engaged sessions that are escalated. An escalated session is an engaged session that is escalated to a human agent.
Abandon rate | The percentage of engaged sessions that are abandoned. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the session.

A blue up-and-down indicator below the value indicates the percent change in a positive direction. A red indicator indicates the percent change in a negative direction.

## Impact summary charts

   > [!div class="mx-imgBorder"]
   > ![Impact summary charts](media/analytics-topic-details-4.PNG)

The Impact summary charts summarize the impact of the topic on key performance indicators for the specified time period.

Description | Details
----------- | -------
Abandon rate impact | The topic's abandon-rate impact score. The abandon-rate impact score is the overall abandon rate including the topic minus the abandon rate excluding the topic.
Resolution rate impact | The topic's resolution-rate impact score. The resolution-rate impact score is the overall resolution rate including the topic minus the resolution rate excluding the topic.
Escalation rate impact | The topic's escalation-rate impact score. The escalation-rate impact score is the overall escalation rate including the topic minus the escalation rate excluding the topic.
CSAT impact | The topic's customer satisfaction impact score. The customer satisfaction impact score is the overall average CSAT survey score including the topic minus the overall average CSAT survey score excluding the topic.

## Topic volume by day chart

   > [!div class="mx-imgBorder"]
   > ![Topic volume by day chart](media/analytics-topic-details-5.PNG)

The topic volume by day chart provides a graphical view of the number of sessions for the topic over the specified time period.
