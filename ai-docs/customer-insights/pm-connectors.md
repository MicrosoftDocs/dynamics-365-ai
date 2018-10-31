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

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

In this section you will learn how to utilize the PBI connector for unlocking the Customer 360 dashboard.

The Customer 360 dashboard enables you to utilize the unified data that you have unlocked through the data configuration process and start visualizing insights around each of your customers. From customer details such as roles and locations, to communication details such as email addresses and phone numbers, to unique KPIs such as Customer Lifetime Spend (LTS) or Engagement Score, many insights are at your fingertips to explore. 

In order to utilize the Customer 360 dashboard make sure that you have created a dataflow and ingested at least one data source to it through the **Data Manager: Get Data** page. Also, make sure you have [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on your computer. Then complete the following steps.

### Step One: Download MEZ File

Along with the offer link, you received a file (MEZ type). Download this file to a location you are familiar with on your desktop.
   
[PBI1]

### Step Two: Publish the Customer 360 Dashboard
 
 1. Bring Customer 360 data to Power BI. Open Power BI for Desktop and select **Get Data** at the top menu.
    
    [PBI2] 
    
 2. Type Customer 360 in the search field, and then select **Customer 360** on the right-side menu. Select **Connect** at the left bottom corner.
    
    [PBI3]
    
3. Publish the Customer 360 dashboard as a service. Insert the following URL into the **URL field**: https://dxt-wus-01.ci.ai.dynamics.com/api/instances/fa252992-8d48-49b3-9d02-06a2ac2a441e/data 

   [PBI4]
     
4. Select **Sign in**.
 
   [PBI5]
     
5. Use your Azure Active Directory credentials, and then select **Connect**.
     
   [PBI6]
     
### Step Three: Create a Customized Dashboard

After completing Step two, you'll see the following:

[PBI7]

1. Choose all the entities around which you want to build your Power BI report. In the example below, the user has chosen two entities:  Customer and Account datasets. Note that the Customer entity is the entity that was created during the data configuration process and that encapsulates the unified customer data that Customer 360 unlocks.
   
   [PBI8]

2. At this point, you are ready to create your customized report using the Power BI left menu. Use the **Filters** fields to produce a report around:

   - A specific customer: Filter by **Customer Name** or **Customer ID**
   - A customer segment: Filter by one or more of the other customer attributes such as gender, location, role, etc.

   [PBI9]

### See also
 [Add a filter to a Power BI service report (in Editing view)](https://docs.microsoft.com/power-bi/power-bi-report-add-filter)<br/>
 [What is Power BI Desktop?](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)
