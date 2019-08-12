---
title: "Power BI connector | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 04/29/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
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
---
# Power BI connector

In this section you will learn how to use the Power BI connector for unlocking the Customer Insights dashboard.

The Customer Insights dashboard enables you to use the unified data that you have unlocked through the data configuration process. From customer details such as roles and locations, to communication details such as email addresses and phone numbers, to unique key performance indicators (KPIs) you might have defined using the **Measures** page (such as Customer Lifetime Spend or Engagement Score), many insights are available. 

In order to use the Customer Insights dashboard, make sure that you have created at least one data source within the **Data sources** page and ingested at least one dataset (entity) into it. Also, make sure you have [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on your computer. Then, complete the following steps.

### Step One: Installing Power BI Connector


<!--from editor: Please check the following download link to make sure it's correct. I wasn't sure if what I saw was what I should see. ("authentication failed") -->


1. Download the custom connector file from [here](https://pbimezfile.blob.core.windows.net/publicpreview/mezfile/Dynamics365CustomerInsights.mez?sp=rl&st=2019-04-03T17:20:30Z&se=2019-08-01T17:20:00Z&sv=2018-03-28&sig=XwuEWCSVk%2F%2BBBbaIZv6mGUmqbSCBPT0rUfHuIVZiLmE%3D&sr=b).
2. Follow steps described [here](https://docs.microsoft.com/power-bi/desktop-connector-extensibility) to install and enable the custom connector.

### Step Two: Publish the Customer Insights dashboard


<!--from editor: Should it be "Microsoft Power BI Desktop" (no "for") in the following sentence? -->

1. Bring Customer Insights data to Power BI: Open Microsoft Power BI for Desktop, and select **Get Data** in the menu at the top of the page.
 
   > [!div class="mx-imgBorder"] 
   > ![Power BI Get Data](media/connector-powerbi-get-data.png "Power BI Get Data")

 
2. Search for **Dynamics 365 Customer Insights (Beta)**, select it from the menu on the right, and then click **Connect** on the lower-right corner.


<!--from editor: The screenshot shows "Customer 360 (Beta)" - is that what we should see? -->

    > [!div class="mx-imgBorder"] 
    > ![Power BI Connector Get Data](media/connector-pbi-step-3.png "Power BI Connector Get Data")

3. If you have not used this connector before, you will need to sign in with the account used by your organization.

4. You will see a list of all the environments you can access. You can select the arrow next to any of the environments to see a full list of entities you can import into:

   > [!div class="mx-imgBorder"] 
   > ![Power BI Connector Navigator](media/connector-pbi-step-4.png "Power BI Connector Navigator")

5. Select the check boxes next to the entities you want to load, and then click **Load** in the lower-right corner of the dialog box. You can select multiple entities from multiple environments.

   > [!div class="mx-imgBorder"] 
   > ![Select check boxes](media/connector-pbi-step-5.png "Select check boxes")

6. You will see the following loading dialog box while your entities are loaded. 

   > [!div class="mx-imgBorder"] 
   > ![Power BI Connector Load](media/connector-pbi-step-6.png "Power BI Connector Load")

### Step Three: Create your report

Once all of your selected entities have loaded, you are ready to create your customized report using the Power BI navigation menu. Use the **Filters** fields to produce a report around:

- A specific customer: Filter by customer name or customer ID.
- A customer segment: Filter by one or more of the other customer attributes (gender, location, or role, for example).
   
### See also


<!--from editor: The first link goes to a page titled "Add a filter to a report in Power BI" - do you want the link text to match? -->

 [Add a filter to a Power BI service report (in Editing view)](https://docs.microsoft.com/power-bi/power-bi-report-add-filter)<br/>
 [What is Power BI Desktop?](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)
