---
title: "Using analytics to improve your virtual agent"
description: "Learn how to use analytics to improve your Dynamics 365 Customer Service virtual agent."
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

# Using analytics to improve your virtual agent

As you create and deploy your virtual agent, you can use analytics to see how your virtual agent is performing. Virtual Agent Designer includes built-in dashboards, interactive charts, and visual filters that give you actionable insights into critical performance metrics, operational data, and emerging trends.

To view the analytics dashboards, select **Analytics** in the navigation pane to open the Analytics page.

   > ![Open Analytics page](media/open-analytics.png)

You can display [Summary](analytics-summary.md), [Engagement](analytics-engagement.md), and [Customer satisfaction](analytics-csat.md) dashboards, or download sessions information by selecting the appropriate tab on the Analytics page.

   > ![Dashboard tabs](media/dashboard-tabs.png)

Some key features of the dashboards include:

* Filters to let you view customer service data for a specific time period.
* Key performance indicator charts that give you the basics of how your system is performing.
* Graphical charts showing trends and breakdowns of cases from a variety of views.
* Impact charts that show the impact and trends of cases related to specific support topics.

## Dashboard filters

Filters on each dashboard let you view support-case information for a specific time period.

   > ![Dashboard filters](media/dashboard-filters.png)

By default, dashboards display information for the last seven days, but you can also display information for the last 30 days by selecting **Last 30 Days**.

## Key performance indicator charts

Key performance indicator charts give you a view of the key performance data for your virtual agent and customer service system for the specified time period. For example, the key performance indicator charts on the Summary dashboard show you:

* The total number of sessions during the period.
* The percentage of total sessions during the period that are engaged sessions.
* The percentage of engaged sessions during the period that are resolved. A resolved session is a session in which customers are offered an end-of-conversation survey.
* The percentage of engaged sessions during the period that are escalated. An escalated session is a session in which a customer requests help from a live agent.
* The percentage of engaged sessions during the period that are abandoned. An abandoned session is an engaged session that is neither resolved nor escalated after one hour from the beginning of the session.

    > ![KPI summary charts](media/summary-charts.png)

Each key performance indicator chart includes an up-and-down indicator next to the value that indicates the percent change in a positive or negative direction over the specified time period.

## Graphical trend and breakdown charts

The dashboards include a variety of graphical charts that give you views of different trends and break down of cases by key criteria such as customer satisfaction, survey response rate, outcomes over time, engagement over time, and daily topic volume.

   > [!div class="mx-imgBorder"]
   > ![Graphical charts](media/engagement-over-time.png)

## Impact charts

Impact charts show you the topics that are having the greatest impact, both positive and negative, on the performance of your virtual agent.

   > [!div class="mx-imgBorder"]
   > ![Impact charts](media/satisfaction-drivers.png)

For details on Dynamics 365 Customer Service Virtual Agent analytics, see the following topics:

* [Analytics overview](analytics-overview.md)
* [Summary dashboard](analytics-summary.md)
* [Engagement dashboard](analytics-engagement.md)
* [Customer satisfaction dashboard](analytics-CSAT.md)
* [Topic details dashboard](analytics-topic-details.md)
* [Download sessions page](analytics-sessions.md)
