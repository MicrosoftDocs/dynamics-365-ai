---
title: "Customer satisfaction dashboard"
description: "Learn the customer service insights available on the Customer satisfaction dashboard​."
keywords: ""
ms\.date: 10/31/2018
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
> ![Customer satisfaction dashboard](media/ai-csi-CSAT-dash.PNG "Customer satisfaction dashboard")

The Customer satisfaction dashboard gives you an overview of customer satisfaction (CSAT), including using artificial intelligence (AI) technology to show you topics that are having the greatest impact on CSAT scores.

The Customer satisfaction dashboard includes a variety of charts with graphical views of your system's customer satisfaction data. For information about each chart, click the link for the chart in the following list, or scroll down to the chart's section below.

* [Total surveys completed](#total-surveys-completed-chart)
* [Survey response rate](#survey-response-rate-chart)
* [Average CSAT](#average-csat-chart)
* [Customer satisfaction breakdown](#customer-satisfaction-breakdown)
* [Top CSAT impactors (AI Insights)](#top-csat-impactors-chart)

The *Top CSAT impactors* chart uses natural language understanding artificial intelligence technology to group support cases as *topics* that are a collection of related cases. This chart shows you the customer support topics that are having the most impact on customer satisfaction, helping you identify areas for improvement that can have the greatest impact on improving the customer's experience.

By default, the dashboard shows you key performance indicators for the last month, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month.

To filter data by product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list. For more information on working with filters, see [Work with dashboards and sample data](use-dashboard-sample-data.md).

## Total surveys completed chart

> [!div class="mx-imgBorder"]
> ![Total surveys completed chart](media/ai-csi-surveys-completed.PNG "Total surveys completed chart")

The total surveys completed chart shows the total number of customer satisfaction surveys completed during the specified time period, and the percent change over the period.

Description | Details
----------- | -------
Total surveys completed | *The number of completed customer satisfaction (CSAT) surveys*

A blue up and down indicator next to the value indicates the percent change in a positive direction. A red indicator indicates the percent change in a negative direction.

## Survey response rate chart

> [!div class="mx-imgBorder"]
> ![Survey response rate chart](media/ai-csi-response-rate.PNG "Survey response rate chart")

The survey response rate chart shows the percentage of customer satisfaction surveys completed during the specified time period, and the percent change over the period.

A blue up and down indicator next to the value indicates the positive percent change in that direction. A red indicator indicates a negative percent change in that direction.

Description | Details
----------- | -------
Survey response rate | *The number of completed customer satisfaction (CSAT) surveys divided by the total number of surveys*

A blue up and down indicator next to the value indicates the positive percent change in that direction. A red indicator indicates a negative percent change.

## Average CSAT chart

> [!div class="mx-imgBorder"]
> ![Average CSAT chart](media/ai-csi-average-csat.PNG "Average CSAT chart")

The average CSAT chart shows the average customer satisfaction survey score during the specified time period, where it falls on the satisfaction scale used in the survey, and the percent change over the period.

A blue up and down indicator next to the value indicates the positive percent change in that direction. A red indicator indicates a negative percent change.

Description | Details
----------- | -------
Average CSAT | *The sum of CSAT scores divided by the count of resolved cases that have CSAT values*

A blue up and down indicator next to the value indicates the positive percent change in that direction. A red indicator indicates a negative percent change.

## Customer satisfaction breakdown

> [!div class="mx-imgBorder"]
> ![Customer satisfaction breakdown](media/ai-csi-csat-breakdown.PNG "Customer satisfaction breakdown")

The customer satisfaction breakdown chart shows the breakdown of customer satisfaction by support channel during the specified time period.

Description | Details
----------- | -------
Customer satisfaction breakdown | *CSAT score breakdown by support channel*

## Top CSAT impactors chart

> [!div class="mx-imgBorder"]
> ![Top CSAT impactors chart](media/ai-csi-CSAT-impactors.PNG "Top CSAT impactors chart")

The top CSAT impactors chart uses artificial intelligence technology to group related support cases as support topics, and then display topics in order of impact the topics are having on customer satisfaction.

Description | Details
----------- | -------
Topic | *Artificial intelligence clustering of cases based on language understanding applied to case titles*
Volume | *The number of cases associated with the topic divided by total cases*
Resolutions | *The number of resolved cases associated with the topic*
Surveys completed | *The count of resolved cases associated with the topic that have CSAT values*
Average CSAT | *The sum of CSAT scores associated with the topic divided by the count of resolved cases associated with the topic that have CSAT values*
Impact | 1 – (*Average CSAT score not including the current topic divided by overall average CSAT score for all topics*)

The chart displays the impact as a red or blue-green bar. The midpoint is the overall average CSAT score. A red bar indicates that the topic's CSAT score is lower than the average CSAT score, resulting in a negative impact on overall customer satisfaction. A blue-green bar indicates that the CSAT score is higher, resulting in a positive impact on overall customer satisfaction. Improving customer satisfaction for the top CSAT topics in red will have the greatest impact on improving overall customer satisfaction.

To see additional information about each topic, right-click the topic name, hover over **Drillthrough**, and then select **Topic Drill Through** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](dashboard-topic-details.md).
