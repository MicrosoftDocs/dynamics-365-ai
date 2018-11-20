---
title: "Power BI | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
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

In this section you will learn how to utilize the **PBI Connector** for unlocking the **Customer 360 Dashboard**.

The Customer 360 Dashboard enables you to utilize the unified data that you have unlocked through the data configuration process and start visualizing insights around each of your customers. From customer's details such as roles and locations, to communication details such as email addresses and phone numbers, to unique KPIs such as Customer Lifetime Spend (LTS) or Engagement Score, many insights are at your fingertips to explore. 

In order to utilize the Customer 360 dashboard make sure that you have created at least one datasource within the **Get Data** page and ingested at least one dataset (entity) into it. Also, make sure you have [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on your computer. Then complete the following steps.

### Step One: Downloading MEZ File

Along with the offer link, you received a file (MEZ type). Download this file to ~\Documents\Power BI Desktop\Custom Connectors

### Step Two: Publishing the Customer 360 Dashboard
 
 1. Bring Customer 360 data to Power BI: Open Power BI for Desktop and select **Get Data** at the top menu.
 
>   [!div class="mx-imgBorder"] 
>   ![](media/connector-powerbi-get-data.png "Power BI Get Data")

 
 2. Type ***Customer 360*** in the search field, and then select **Customer 360** on the right-side menu. Lastly, Select **Connect** at the left bottom corner:

    > [!div class="mx-imgBorder"] 
    > ![](media/connector-pbi-step-3.png "Power BI Connector")

3. Publish the Customer 360 dashboard as a service: 
- You will need to copy your instance ID (can be taken from your app URL) and attach it to the following address:
  https://tip.api.ci.ai.dynamics.com/api/instances/**your instance ID**

- Then copy paste the complete URL address (fixed part + **your instance ID**) to the URL field in Power BI as shown below:

  > [!div class="mx-imgBorder"] 
  > ![](media/connector-copy-instanceid.png "Copy Instance ID")

4. Select **Sign in**.

  > [!div class="mx-imgBorder"] 
  > ![](media/connector-sign-in.png "Sign in to Customer 360")
     
5. Use your Azure Active Directory credentials, and then select **Connect** as shown in red below:
     
  > [!div class="mx-imgBorder"] 
  > ![](media/connector-sign-in-azure-credentials.png "Sign in using Azure credentials")
     
### Step Three: Creating a Customized Dashboard

After completing Step two, you'll get to the following screen:

> [!div class="mx-imgBorder"] 
> ![](media/connector-now-signed-in.png "Signed in to Customer 360")

1. Choose all the entities around which you want to build your Power BI report. In the example below, the user has chosen the **Conflated Match Pairs** entity. Note that this entity is the entity that was created during the data configuration process and that encapsulates your unified customer data. You may want to include that entity to extract the most insightful observations from your data.
   
   > [!div class="mx-imgBorder"] 
   > ![](media/connector-conflated-match-pairs.png "Conflated match pairs")


2. At this point, you are ready to create your customized report using the Power BI left menu. Use the **Filters** fields to produce a report around:

   - A specific customer: Filter by **Customer Name** or **Customer ID**
   - A customer segment: Filter by one or more of the other customer attributes such as gender, location, role, etc.
   
### See also
 [Add a filter to a Power BI service report (in Editing view)](https://docs.microsoft.com/power-bi/power-bi-report-add-filter)<br/>
 [What is Power BI Desktop?](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)
