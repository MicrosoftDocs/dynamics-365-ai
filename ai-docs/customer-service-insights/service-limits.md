---
title: "Service limits in Dynamics 365 Customer Service Insights"
description: "Understand limits and restrictions within the Dynamics 365 Customer Service Insights product."
keywords: ""
ms.date: 12/08/2021
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

This article describes the built-in limits for the Customer Service Insights service, which are designed to ensure the reliability and stability of the service. Any requests for changes can be made through the [Ideas forum](https://go.microsoft.com/fwlink/?linkid=2024757). 

## Service limits

The following table lists the built-in limits for the embedded version of insights in Customer Service Hub and Customer Service workspace.
 
| Area  | Limits  | Notes |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Data age limit | 24-month period | Reports are limited to case data from the last 24 months. |
| Dashboard interactions | No limit | No limits on the number of interactions or drill-throughs within reports. |
| Topics | At least three related cases | Topics require at least three semantically related cases for the model to generate topics. |
| Topics refresh | 100k per run | Refresh of topics uses up to 100,000 cases or conversations per run. |
| Data refresh | Once every 24 hours | Data refresh occurs automatically each day, starting at midnight UTC. The time when the refresh completes is not guaranteed. For more information, see [Information you need to know about Customer Service analytics reports](/dynamics365/customer-service/customer-service-analytics-insights-csh#information-you-need-to-know-about-customer-service-analytics-reports). |
| AI suggestions for active cases | Each user license adds 30 active cases where agents can get AI suggested knowledge articles and similar cases in real-time. |
|AI suggestions for conversations | 150 conversations/month per user license | Each user license adds 150 Omnichannel conversations where agents can get AI suggested knowledge articles and similar cases in real-time. |


## Service protection limits for AI suggestions

AI suggestions for Case and Knowledge are available, and we're introducing service protection limits on these capabilities to maintain a consistent quality of service for all our customers, but there is no penalty if customers exceed pre-defined limits. Over time, Microsoft may adjust these limits in keeping with customer usage patterns and provide options for customers with high usage scenarios and patterns to purchase additional capacity in a manner minimally disruptive to those customers.

The service protection limits for AI suggestions are defined below. The total limits are pooled at the tenant level based on the number of Customer Service Enterprise user licenses available in the tenant. For more information about AI suggestions, see [Enable AI suggestions for similar cases and knowledge articles](/dynamics365/customer-service/csw-enable-ai-suggested-cases-knowledge-articles).

## Impact on Power Platform Capacity

Enabling the insights feature will impact Dataverse entitlements. For more information, see [New Microsoft Dataverse storage capacity](/power-platform/admin/capacity-storage).


### See also
[Customer Service historical analytics](/dynamics365/customer-service/configure-cs-historical-analytics-csh)<br>
[Topic clustering for cases](/dynamics365/customer-service/configure-topics-clustering-cases-cs)<br>
[Customer Service Analytics in Power BI](/dynamics365/customer-service/configure-customer-service-analytics-dashboard)<br>
[Knowledge search analytics](/dynamics365/customer-service/enable-knowledge-search-insights)<br>
[AI suggestions for similar cases and knowledge articles](/dynamics365/customer-service/csw-enable-ai-suggested-cases-knowledge-articles)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
