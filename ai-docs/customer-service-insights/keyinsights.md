---
title: "Use homepage to discover AI generated insights"
description: "Easily discover AI insights using Customer Service Insights homepage"
keywords: ""
ms.date: 1/14/2020
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: alicelu
ms.author: alicelu
manager: shellyha
ms.reviewer: alicelu
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Discover key insights from your customer service data

The homepage (preview) of Dynamics 365 Customer Service Insights presents insights from your customer service data in a visually rich way, making it easier to discover topic issues to focus on and why they are suggested. 

<insert header screenshot>
  
At the top of the page, you can find workspace information on nubmer of case data imported, number of topics discovered, and percentage of cases that were successfully clusterd to find the topics. 
* **Workspace:**  name of your environment with your customer service data.
* **Case collected:** number of total cases imported into this workspace, using the method of all cases created in the last 60 days or up to 1 million cases, whichever's great. See more details around limits [here](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/service-limits).
* **Topics:** number of topics discovered from percentage of total imported cases that were successfully clustered based on semantic similarity. If no topics are discovered, it could be caused by multiple reasons such as not enough case data in the workspace, or clustering is still in progress. Find more troubleshooting details [here](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/topics-page#troubleshooting-empty-topics-page).
* **Time period selectors:** enable comparison between the selected time period and the previous period to see how KPIs are changing over time as well as across different time ranges. The default selection is "Last 7 days", based on the creation date of cases imported since the last refresh. 
  * Last 24 hours
  * Last 7 days
  * Last 30 days
* **Time period range:** based on the selected time period, this shows the time range (in UTC time zone) of the imported cases that were used to discover topic issues shown on the page.  
* **Refreshed date:** this timestamp indicates when the workspace was last refreshed, cases created up until the last refresh date are imported to the workspace, which are used to calculate AI and BI insights. 

## Topics to watch 
<screenshot>
Topics ranked high across these 3 key areas are shown in **Topics to watch** to make it easier for customer service managers to discover top issues:
  
  * **Volume driver:** Topics with the largest volume of cases created in the selected time period.
  * **Negative CSAT impact:** Topics that have the most negative impact on your total CSAT score. CSAT is data collected from surveys.
  * **Emerging rate:** Get a "heads-up" on topics with high rate of new incoming cases in the selected time period.

<screenshot>
Clicking on the light bulb icon will display a quick inline explanination on the reason behind showing these topics, as well as recommendations on possible actions to take. 

## Topics with longest average resolution time
<Topcis with longest average resolution time>

Why this matters
Identifying these topics will help your team focus on issues that are taking a long time to resolve. Agents with the longest and shortest resolution times in those topics are highlighted to suggest potential training opportunities.

Recommendation
Empower agents performing well in a topic to coach agents who are taking longer than average to resolve similar.
<Consider automatin these topics>
  
<Topics impacting CSAT by channel>
  
<Peak time with high case volume>
### 
Iof the concept of "cards" that highlights key topics to watch across various analytics dimensions. It

## Compare time range

<insert workspace info screenshot>
  
<insert time period selector screenshot>
  
