---
title: "Export data from Customer Service Insights"
description: "Export data from Customer Service Insights"
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

# Export data from Customer Service Insights

Customer Service Insights now offers a way for you to get AI and BI insights outside of the out-of-box dashboards automatically created in the workspace. 

To access the option to export your Customer Service Insights data:
1. Go to **Settings**

    ![Settings - export data](media/exportdata_settings.png)

2. Click on **Export data**, it will open up the Export data window where you can choose the method of export.

    ![Export data using web api](media/exportdata_webapi.png)

3. Click on **Generate url** to create a new Web API endpoint to get the exported data, use the copy icon on the right to easily get the full url. 
4. **Delete url** will disable the previously generated url from being accessible. You can always generate a new url after deletion. 

Currently the ability to export data via Web API is in preview. 

Soon, the ability to export via connectors from Power BI, Power Apps, and Power Automate will be supported.

## Data fields exported

The Web API endpoint will export all the data fields listed below, given they are available in your workspace. It's possible that some workspaces won't have all the fields listed below if they aren't applicable or configured correctly in data mapping. Lear more about custom data entity/field mapping [here](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/map-data).

**Case data**
 - Case title
 - Created date
 - Modified date
 - Resolved date
 - Escalated on date
 - Is escalated
 - Business Unit
 - Priority
 - State
 - Assigned agent name
 - Team
 - Product
 - CSAT score (1-5 scale)
 - Origin channel
 - Resolve by SLA
 - Case number

**Generated data**
- Topic
- Is topic popular
- Topic id
- Relevance score

The full list of entities and fields used by Customer SErvice Insights is documented [here](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/customer-service-entities).


## Considerations
* Before sharing the exported data with others, be sure you have the right permissions to share the data and the sharee can access the data. 
* The exported data are refreshed with the typical workspace refresh schedule on a daily basis. Workspace refresh will be temporarily paused due to inactivity after 30 days, which will also lead to the exported data being stale. 
* If you suspect the url may be leaked, simply delete the url and generate it again, which will disable the old url to prevent it from being used. 
* Rate limits for accessing the API for every IP address: 
  * 5 times per minute
  * 20 times per hour
  * 100 times per day

