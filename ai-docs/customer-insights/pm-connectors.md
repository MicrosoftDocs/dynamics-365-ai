---
title: "Power BI connector | Microsoft Docs"
description: "Learn how to use the Dynamics 365 Customer Insights connector in Power BI."
ms.date: 12/04/2019
ms.reviewer: groxer
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Power BI connector

In  this section you will learn how to use the Dynamics 365 Customer Insights connector in Power BI to combine Customer Insights unified data with Power BI’s data visualization capabilities.

The Customer Insights connector enables you to use the unified data that you have unlocked through the data configuration process. This includes customer details such as roles and locations and unique key performance indicators (KPIs) you might have defined using the **Measures** page (such as Customer Lifetime Spend or Engagement Score).

In order to see your customer insights in Power BI, make sure that you have created at least one data source within the **Data sources** page and ingested at least one dataset (entity) into it. Also, make sure you have [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed on your computer. Then, complete the following steps.

1. Open Microsoft Power BI Desktop and select **Get Data** in the menu at the top of the page.

2. Search for **Dynamics 365 Customer Insights**, select it from the menu on the right, and then select **Connect** on the lower-right corner.

3. If you have not used this connector before, you will need to sign in with the same account you use to view the data in Customer Insights.

4. You will see a list of all the environments you can access. You can select the arrow next to any of the environments to see a full list of entities you can import.

   > [!div class="mx-imgBorder"]
   > ![Power BI Connector Navigator](media/connector-pbi-step-4.png "Power BI Connector Navigator")

5. Select the check boxes next to the entities you want to load, and then select **Load** in the lower-right corner of the dialog box. You can select multiple entities from multiple environments.

6. You will see a loading dialog box while your entities are loaded. Once all of your selected entities have loaded, you'll have the capabilities of Power BI combined with your data from Customer Insights.

## See also

 [Add a filter to a Power BI service report (in Editing view)](https://docs.microsoft.com/power-bi/power-bi-report-add-filter)

 [What is Power BI Desktop?](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)
