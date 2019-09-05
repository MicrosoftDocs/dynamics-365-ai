---
title: "Power BI connector | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 08/21/2019
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

In  this section you will learn how to use the Customer Insights connector in Power BI to combine Customer Insights unified data with Power BI’s data visualization capabilities.

The Customer Insights connector enables you to use the unified data that you have unlocked through the data configuration process. This includes customer details such as roles and locations and unique key performance indicators (KPIs) you might have defined using the **Measures** page (such as Customer Lifetime Spend or Engagement Score). 

In order to see your customer insights in Power BI, make sure that you have created at least one data source within the **Data sources** page and ingested at least one dataset (entity) into it. Also, make sure you have [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on your computer. Then, complete the following steps.


1. Open Microsoft Power BI Desktop and select **Get Data** in the menu at the top of the page.

   > [!div class="mx-imgBorder"] 
   > ![Power BI Get Data](media/connector-powerbi-get-data.png "Power BI Get Data")
 
2. Search for **Dynamics 365 Customer Insights (Beta)**, select it from the menu on the right, and then click **Connect** on the lower-right corner.

    > [!div class="mx-imgBorder"] 
    > ![Power BI Connector Get Data](media/connector-pbi-step-3.png "Power BI Connector Get Data")

3. If you have not used this connector before, you will need to sign in with the same account you use to view the data in Dynamics 365 Customer Insights.

4. You will see a list of all the environments you can access. You can select the arrow next to any of the environments to see a full list of entities you can import into:


   > [!div class="mx-imgBorder"] 
   > ![Power BI Connector Navigator](media/connector-pbi-step-4.png "Power BI Connector Navigator")

5. Select the check boxes next to the entities you want to load, and then click **Load** in the lower-right corner of the dialog box. You can select multiple entities from multiple environments.

   > [!div class="mx-imgBorder"] 
   > ![Select check boxes](media/connector-pbi-step-5.png "Select check boxes")

6. You will see the following loading dialog box while your entities are loaded. 

   > [!div class="mx-imgBorder"] 
   > ![Power BI Connector Load](media/connector-pbi-step-6.png "Power BI Connector Load")

Once all of your selected entities have loaded, you'll have the capabilities of Power BI combined with your data from Dynamics 365 Customer Insights!

### See also
 [Add a filter to a Power BI service report (in Editing view)](https://docs.microsoft.com/power-bi/power-bi-report-add-filter)<br/>
 [What is Power BI Desktop?](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)
