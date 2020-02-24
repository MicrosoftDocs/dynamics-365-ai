---
title: "Export data from Dynamics 365 Customer Service Insights"
description: "Export data with an API endpoint URL so you can get further insights into your data beyond the default dashboards."
keywords: ""
ms.date: 2/24/2020
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: iaanw
ms.author: iawilt
manager: shellyha
ms.reviewer: alicelu
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Export data from Dynamics 365 Customer Service Insights

[!INCLUDE[cc-beta-prelease-disclaimer.md](../includes/cc-beta-prerelease-disclaimer.md)]

Dynamics 365 Customer Service Insights enables you to export your data to a web API endpoint.

You can then query the API for additional insights that go beyond the [default dashboards](dashboard-overview.md). 

1. Go to **Settings**.

    ![Settings - export data](media/exportdata_settings.png)

2. Select **Export data**. You see the Export data window where you choose the export method.

    ![Export data using web api](media/exportdata_webapi.png)

3. Select **Generate URL** to create a new web API endpoint for the exported data, which you can copy to the clipboard. 

**Delete URL** disables any previously generated URL. You can then generate a new URL. 


## Exported data fields 

The web API endpoint includes the following if they're available in your workspace. 

Fields that aren't applicable or are mapped incorrectly may not be listed in some workspaces.

More information: [Map your data to custom entities and fields](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/map-data)

**Case data**
 - Case title
 - Created date
 - Modified date
 - Resolved date
 - Escalated on date
 - Is escalated
 - Business unit
 - Priority
 - State
 - Assigned agent name
 - Team
 - Product
 - CSAT score (1-5 scale)
 - Origin channel
 - Resolve by SLA
 - Case number

**Created data**
- Topic
- Is topic popular
- Topic ID
- Relevance score

More information: [Dynamics 365 Customer Service entities used by Customer Service Insights](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/customer-service-entities)


## Considerations
* Before sharing the exported data with others, check that you and the people you're sharing with have the correct permissions. 

* The exported data is refreshed daily, following the typical workspace refresh schedule.  Exported data isn't refreshed if a workspace refresh is temporarily paused because of inactivity after 30 days.

* If you suspect the URL has been inappropriately shared, delete the URL and generate a new one. This action disables the old URL and prevents it from being used. 

* Rate limits for accessing the API for every IP address are: 
  * Five times per minute
  * 20 times per hour
  * 100 times per day

* Rate limits for accessing the API for every key as the parameter of that API are:
  * Five times per minute
  * 20 times per hour
  * 100 times per day
