---
title: "Service limits in Dynamics 365 Customer Service Insights"
description: "Understand limits and restrictions within the Dynamics 365 Customer Service Insights product."
keywords: ""
ms.date: 10/22/2020
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid:
author: lalexms
ms.author: laalexan
manager: shujoshi
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150

---

# Service limits in Dynamics 365 Customer Service Insights

This article describes the built-in limits to the Customer Service Insights service, which are designed to ensure the reliability and stability of the service. Any requests for changes can be made through the [Ideas forum](https://go.microsoft.com/fwlink/?linkid=2024757). 

The following tables outline the limits based on the insights version you are using:

- [Embedded Customer Service Hub and Customer Service workspace limits](#embedded-customer-service-insights-limits)
- [Standalone app limits](#standalone-customer-service-insights-app-limits)

## Embedded Customer Service Insights limits

This following table lists the built-in limits for the embedded version of insights in Customer Service Hub and Customer Service workspace.
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Date retention | 24-month data retention limit | Reports are limited to case data from the last 24 months. |
| Dashboard interactions | No limit | No limits on the number of interactions or drill-throughs within reports. |
| Topics | At least three related cases | Topics require at least three semantically related cases for the model to generate topics. |
| Data refresh | Once every 24 hours | Data refresh occurs automatically each day, starting at midnight UTC. The time when the refresh completes is not guaranteed. For more information, see [Information you need to know about Customer Service analytics reports](https://docs.microsoft.com/dynamics365/customer-service/customer-service-analytics-insights-csh#information-you-need-to-know-about-customer-service-analytics-reports). |


## Standalone Customer Service Insights app limits

This following table lists the built-in limits for the Customer Service Insights standalone app.
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Data import | Cases created in the last 60 days, or 1 million cases. | The date a case was created is determined by the field in Common Data Service (CDS) which the [“Created On” field is mapped to](map-data.md). Cases created on the same day will also be imported when a workspace is created or refreshed. The total import counts towards the 1 million case limit. If a workspace refresh exceeds this limit then the cases created most recently will be imported.<br> <br> The number of cases that can be imported is determined by your organization's licensing. See [Licensing and case-capacity considerations](licensing-case-capacity.md) for details. |
| Automatic data refresh | Once every 24 hours | Automatic data refresh occurs automatically, starting at midnight UTC. The time when the refresh completes is not guaranteed. |
| Manual data refresh | On-demand data refresh is allowed up to 10 times per day. | After the limit is reached, you need to wait for the automatic refresh to occur for the manual refresh limit to reset. For more information about the manual data refresh, see [Trigger a refresh of your Customer Service Insights data](trigger-refresh.md).  |
| Data location | Data is located in the same region as the Dynamics 365 environment the data is connected to.     | Geographical location of data occurs automatically and cannot be controlled by users at this time. |
| Dashboard interactions | None | There are no limits on the number of interactions allowed on dashboards, such as cross filtering or drillthrough. |
| Connecting to a Dynamics 365 environment | One workspace per Dynamics 365 environment per user | A Dynamics 365 environment cannot be connected with multiple workspaces at the same time by the same user. If a workspace is created and then deleted, it can be connected  again. <br> <br> In addition, a single workspace cannot be connected to more than one Dynamics 365 environment. |
| Topics generated from cases | Topics are generated only from cases for which there are at least three related cases.| Because topics are automatically created based on similar customer service cases, the system needs a minimum number of cases to create a topic. <br> <br> In order for topics to be meaningful, we recommend having at least 1,000 cases.|
