---
title: "Engagement dashboard"
description: "Learn about the AI for Customer Service Virtual Agent Engagement dashboard."
keywords: ""
ms.date: 1/14/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Engagement dashboard

   > [!div class="mx-imgBorder"]
   > ![Engagement dashboard](media/analytics-engagement-1.PNG)

The Engagement dashboard provides a focused view of engagement metrics and trends. It includes charts that provide graphical views of the breakdown of session outcomes and engagements over time. For information about each chart, select the link for the chart in the following list, or scroll to find the section about the chart later in this topic:

* [Session outcomes over time chart](#session-outcomes-over-time-chart)
* [Engagement over time chart](#engagement-over-time-chart)

By default, the dashboard shows you key performance indicators for the last seven days. To change the time period to the last 30 days, select **Last 30 days** from the drop-down list at the top of the dashboard.

## Session outcomes over time chart

   > [!div class="mx-imgBorder"]
   > ![Session outcomes over time chart](media/analytics-engagement-2.PNG)

The Session outcomes over time chart provides a graphical view of the daily resolution rate, escalation rate, and abandon rate over the specified time period.

Description | Details
----------- | -------
Resolved | The daily rate of resolved sessions. A resolved session is an engaged session in which the user receives a customer satisfaction (CSAT) survey and either does not respond or responds *Yes*.
Escalated | The daily rate of escalated sessions. An escalated session is an engaged session that is escalated to a human agent.
Abandoned | The daily rate of abandoned sessions. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the session.

## Engagement over time chart

   > [!div class="mx-imgBorder"]
   > ![Outcomes over time chart](media/analytics-engagement-3.PNG)

<!--note from editor: Line 47: "An engaged session is either a session in which a user-created topic is triggered or a session that continues as an escalation" ?-->

The Engagement over time chart provides a graphical view of the number of engaged and unengaged sessions over time. An engaged session is a session in which a user-created topic is triggered, or the session ends in escalation.

Description | Details
----------- | -------
Engaged | The daily number of engaged sessions.
Unengaged | The daily number of unengaged sessions.
