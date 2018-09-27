---
title: "Customer Satisfaction dashboard "
description: "Learn the customer service insights available on the Customer Satisfaction dashboard​."
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

# Customer Satisfaction dashboard

![Customer Satisfaction dashboard](media/ai-csi-CSAT-dash.png)

The Customer Satisfaction dashboard gives you an overview of customer satisfaction with their support experience during the specified time period.

You can display [KPI Summary](ai-csi-dash-kpi-summary.md), [Incoming Cases](ai-csi-dash-incoming-cases.md), [Case Resolutions](ai-csi-dash-case-resolutions.md), and Customer Satisfaction dashboards by clicking each dashboard's icon in the navigation pane. You can display the [Topic Details](ai-csi-dash-topic-details.md) dashboard by right-clicking a topic in one of the AI Insights charts in those dashboards. The KPI Summary dashboard is the default Dynamics 365 AI for Customer Service dashboard.

The Customer Satisfaction dashboard provides graphical views of customer satisfaction survey results, including:

* The total number of surveys completed.
* The survey response rate.
* The average customer satisfaction (CSAT) score.
* The survey responses by location.

In addition, the dashboard uses artificial intelligence technology to categorize customer support cases by topic and show you the topics that are having the greatest impact on customer satisfaction. This can help you identify areas for improvement that can have the greatest impact on customer satisfaction.

By default, the dashboard shows you key performance indicators for the last week, and for all products, channels, business units, and teams in your system. To change the time period, select a value from the Time Period drop-down list at the top of the dashboard. You can select either last day, last week, or last month. To display data for a specific product, channel, business unit, or team, select a value from the Product, Channel, Business Unit, or Team drop-down list.

## Total surveys completed chart

![Total surveys completed chart](media/ai-csi-surveys-completed.png)

The total surveys completed chart shows the total number of customer satisfaction surveys completed during the specified time period, and the percent change over the period.

## Survey response rate chart

![Survey response rate chart](media/ai-csi-response-rate.png)

The survey response rate chart shows the percentage of customer satisfaction surveys completed during the specified time period, and the percent change over the period.

## Average CSAT chart

![Average CSAT chart](media/ai-csi-average-csat.png)

The Average CSAT chart shows the average customer satisfaction survey score during the specified time period, where it falls on the satisfaction scale used in the survey, and the percent change over the period.

## Survey responses by city chart

![Survey responses by city chart](media/ai-csi-responses-by-city.png)

The survey responses by city chart shows the geographical location of customer satisfaction surveys completed during the specified time period.

## Top CSAT impactors chart (AI Insights)

![Top CSAT impactors](media/ai-csi-CSAT-impactors.png)

The top CSAT impactors chart uses artificial intelligence technology to group related support cases as support topics, and then display topics in order of impact the topics are having on customer satisfaction, showing:

* The percentage of total case volume for the topic.
* The number of support cases.
* The number of customer satisfaction surveys completed.
* The average CSAT score.
* The impact on the average CSAT score.

The chart displays the impact as a red or blue bar:

* A red bar indicates that the topic is having a negative effect on customer satisfaction. It represents the percent change in average CSAT score if that topic's cases are not included in calculating the CSAT score.
* A blue bar indicates that the topic is having a positive effect on customer satisfaction. It represents the negative percent change in average CSAT score if that topic's cases are not included in calculating the CSAT score.

Improving case resolution time for the top CSAT topics in red will have the greatest impact on improving overall customer satisfaction.

To see additional information about each topic, right-click the topic name and select **Drillthrough** to display the Topic Details dashboard. For more information, see [Topic Details Dashboard](ai-csi-topic-details.md).