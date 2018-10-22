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
# Customer 360 Dashboard

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

**This dashboard encapsulates everything that you need to know about each of your customers**. From Customer detials such as rule and address, to communication details such as email address and phone number, to KPIs that were calaculated specifically for that customer, to other important customer-level insights that are important for your business health. 

In order to utilize the Customer 360 dashboard make sure that you have created a dataflow and ingested at least one datasource to it through the **Data Manager: Get Data** page (otherwise you should first review the Data Manager section). Lastly, make sure you have **Power BI Desktop** and **Gateway Windows Server** on your computer or else you will need to install both using the following links:
- **Power BI Desktop:**
- **Gateway Windoes Server:**

Then complete those few steps:
- **Step One: Downloading a PBI Connector**: 
    - **Downloading MEZ File**: Along with the Offer link you have received a file (from a MEZ type). Download this file to a location you are familiar with in your desktop.
    - **Authorizing the File**: Next you want to authorize this file using the **Gateway Windows Server**. This gateway authorizes files for power BI where you will view the Customer 360 dashboard. To authorize, you should open the Gateway, go to **Connectors** in the left menu (shown below in red), and search for the MEZ file you have downloaded in the previous step (shown in green). Lastly, hit **Save** (shown in blue):
[]

- **Step Two: Publishing the Customer 360 Dashboard**: 
    - **Bringing Customer 360 data to Power BI**: Open Power BI for Desktop and click **Get Data** at the top menu. That will open the window that is shown below. Then, type **"Customer 360"** in the search field (shown in red) and choose **Customer 360** on the right-side menu (shown in blue). Lastly, click **Connect** at the left bottom corner of the window. 
    - **Publishing the Customer 360 Dashboard as a Service**: Upon completing the previous step you will get the following window:
    []
    
     You should insert the following URL into the **url field** that is shown above: 
     https://apiapi.ci.ai.instances/a73a8b95-484f-4913-9a62-76417b543b7d/data/ 
     
     https://dev.api.ci.ai.dynamics-int.com/app/configuration/map?instanceId=b934bbd7-1e37-41d8-843e-5850bdb4d747
     
     Lastly, **provide your AAD credentials** within the screen that is shown below:
     []
     
- **Step Three: Creating a Customized Dashboard:
Upon completing step two you will get to the following screen:
[]

Here you can start creating your customized dashboard by using the right menu. Use the **Filters** fields as shown below to produce a dashbaord around:
- A specific customer by filtering by the **Customer Name** or **Customer ID** (as examplified below)
- A customer segment by filtering by one or more of the other customer attributes such as gender, location, role, etc
[]


It includes four major parts: The Customer Card, selected customer KPIs, top interests and brands for customers that are like this customer, and this customer's activities. 
- **Customer Card:** This card is the same card that appears for that customer on the *Profile* page that was described earlier.
- **Customer KPIs**: The most insightful key performance indicators (KPIs) across the four customer journey phases:
  - **Awereness KPIs:**
      - sdf
      - sdf
  - **Engagement KPIs:**
      - Engagement score
      - sdf
  - **Fulfillement KPIs:** 
      - Sales
      - Sales in Process
      - Lifetime spend 
  - **Service KPIs:**
      - Number of active cases
      - dsfd
