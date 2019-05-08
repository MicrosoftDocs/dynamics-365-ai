---
title: "Power BI connector | MicrosoftDocs"
description: 
ms.custom: ""
<<<<<<< HEAD
ms.date: 04/04/2019
=======
ms.date: 04/29/2019
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1
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

1. Download the custom connector file from [here](https://pbimezfile.blob.core.windows.net/publicpreview/mezfile/Dynamics365CustomerInsights.mez?sp=rl&st=2019-04-03T17:20:30Z&se=2019-08-01T17:20:00Z&sv=2018-03-28&sig=XwuEWCSVk%2F%2BBBbaIZv6mGUmqbSCBPT0rUfHuIVZiLmE%3D&sr=b).
2. Follow steps described [here](https://docs.microsoft.com/power-bi/desktop-connector-extensibility) to install and enable the custom connector.

<<<<<<< HEAD
## Step Two: Publish the Customer Insights dashboard
 
1. Bring Customer Insights data to Power BI. Open Microsoft Power BI for Desktop, and select **Get Data** in the menu at the top of the page.
=======
### Step Two: Publish the Customer Insights dashboard
 
1. Bring Customer Insights data to Power BI: Open Microsoft Power BI for Desktop, and select **Get Data** in the menu at the top of the page.
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1
 
   > [!div class="mx-imgBorder"] 
   > ![](media/connector-powerbi-get-data.png "Power BI Get Data")

 
<<<<<<< HEAD
 2. Type **Customer Insights** in the search field, and then select **Customer Insights** on the right-side menu. Select **Connect** in the lower-left corner.
=======
2. Search for **Dynamics 365 Customer Insights (Beta)**, select it from the menu on the right, and then click the Connect button in  the lower-righthand corner.
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1

    > [!div class="mx-imgBorder"] 
    > ![](media/connector-pbi-step-3.png "Power BI Connector Get Data")

<<<<<<< HEAD

3. **Create a report in Power BI**
Paste your environment API URL in the URL field shown below to connect to your Customer Insights environment. 

To get the environment API URL do the following: 
- Use the Global APIs found here:  https://global.api.ci.ai.dynamics.com/swagger.  Then execute the /api/instances under the “Instances” section after you authorize.  This will return all the environment for the user. 

- For the environment of interest, review the return package which includes a ScaleUnitUri. You need to use this ScaleUnitUri to create the environment API URL that is required to connect from PBI.  In order to do this, append /api/instances/**your environment ID**/Data to the ScaleUnitUri. Hence if the ScaleUnitUri returned for your environment is https://prod-wus-01.api.ci.ai.dynamics.com then the URL to use in Power BI is: https://prod-wus-01.api.ci.ai.dynamics.com/api/instances/<EnvironmentID>/data

   > [!div class="mx-imgBorder"] 
    > ![](media/connector-copy-instanceid.png "Copy Instance ID")
=======
3. If you have not used this connector before, you will need to sign-in with the account used by your organization.

4. You will be brought to a list of all of the environments you have access to. You can select the arrow next to any of the environments to see a full list of entities you can import into :

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-pbi-step-4.png "Power BI Connector Navigator")
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1

5. Select the checkboxes next to the entities you want to load, and then click the Load button in  the bottom-righthand corner of the dialog box. You can select multiple entities from multiple environments.

   > [!div class="mx-imgBorder"] 
<<<<<<< HEAD
   > ![](media/connector-sign-in.png "Sign in to Customer Insights")
     
5. Use your Azure Active Directory credentials, and then select **Connect**, as in the following example.

   > [!div class="mx-imgBorder"] 
   > ![](media/connector-sign-in-azure-credentials.png "Sign in using Azure credentials")
     
## Step Three: Create a customized dashboard

After completing Step Two, you'll get to the following screen.
=======
   > ![](media/connector-pbi-step-5.png "Power BI Connector Navigator")
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1

6. You will be brought to the following loading dialog box while your entities are loaded. 

<<<<<<< HEAD
Follow these steps to create a customized dashboard:

1. Choose all the entities around which you want to build your Power BI report. In the following example, the user has chosen the Conflated Match Pairs entity. Note that this entity is the entity that was created during the data configuration process and that it encapsulates your unified customer data. 

=======
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1
   > [!div class="mx-imgBorder"] 
   > ![](media/connector-pbi-step-6.png "Power BI Connector Load")

### Step Three: Create your report

<<<<<<< HEAD
2. At this point, you are ready to create your customized report using the Power BI navigation menu. Use the **Filters** fields to produce a report around:

   - A specific customer: Filter by customer name or customer ID.
   - A customer segment: Filter by one or more of the other customer attributes (gender, location, or role, for example).
=======
Once all of your selected entities were loaded, you are ready to create your customized report using the Power BI navigation menu. Use the **Filters** fields to produce a report around:

- A specific customer: Filter by customer name or customer ID.
- A customer segment: Filter by one or more of the other customer attributes (gender, location, or role, for example).
>>>>>>> 9038288590d9c0ede6e36a98eef443aa9aa336f1
   
### See also
 [Add a filter to a Power BI service report (in Editing view)](https://docs.microsoft.com/power-bi/power-bi-report-add-filter)<br/>
 [What is Power BI Desktop?](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)
