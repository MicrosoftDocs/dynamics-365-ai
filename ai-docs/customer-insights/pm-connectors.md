---
title: "Power BI | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/31/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# PBI Connector
**The 

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

**In this section you will learn how to utilize the PBI connector for unlocking the Customer 360 Dashboard.** 

**The Customer 360 Dashboard** enables you to utilize the unified data that you have unlocked through the **Data Configuration** process and start visualize insights around each of your customers. From Customer details such as roles and locations, to communication details such as email addresses and phone numbers, to unique KPIs such as Customer Lifetime Spend (LTS) or Engagmenet Score, many insights are now at your fingertips to explore. 

In order to utilize the Customer 360 dashboard make sure that you have created a dataflow and ingested at least one datasource to it through the **Data Manager: Get Data** page (otherwise you should first review the Data Manager section). Lastly, make sure you have **Power BI Desktop** on your computer (free):
- **Link to downloading Power BI for Desktop:** https://powerbi.microsoft.com/en-us/desktop/

Then complete those few steps:
- **Step One: Downloading MEZ File**: Along with the Offer link you have received a file (from a MEZ type). Download this file to a location you are familiar with in your desktop.
   
[]

- **Step Two: Publishing the Customer 360 Dashboard**: 
    - **Bringing Customer 360 data to Power BI**: Open Power BI for Desktop and click **Get Data** at the top menu. That will open the window that is shown below. Then, type **"Customer 360"** in the search field (shown in red) and choose **Customer 360** on the right-side menu (shown in blue). Lastly, click **Connect** at the left bottom corner of the window (shown in green).
    []
    
    - **Publishing the Customer 360 Dashboard as a Service**: Upon completing the previous step you will get the following window:
    []
    
     You should insert the following URL into the **url field** that is shown above: 
     https://dxt-wus-01.ci.ai.dynamics.com/api/instances/fa252992-8d48-49b3-9d02-06a2ac2a441e/data 

     Lastly, **provide your AAD credentials** within the screen that is shown below:
     []
     
- **Step Three: Creating a Customized Dashboard:**
Upon completing step two you will get to the following screen:
[]

Here you can start creating your customized dashboard by using the right menu. Use the **Filters** fields as shown below to produce a dashbaord around:
- A Specific Customer: Filter by the **Customer Name** or **Customer ID** (as examplified below in red)
- A Customer Segment: Filter by one or more of the other customer attributes such as gender, location, role, etc (shown in blue)
[]

**If you are less familiar with how to filter in Power BI for Desktop**, you might want to explore the following documentation:**
https://docs.microsoft.com/en-us/power-bi/power-bi-report-add-filter

**If you want to learn more on Power BI for Desktop**, you can utilize the following documentation:**
https://docs.microsoft.com/en-us/power-bi/desktop-what-is-desktop

