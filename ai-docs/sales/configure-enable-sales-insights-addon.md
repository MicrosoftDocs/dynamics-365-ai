---
title: "Configure and enable Sales insights add-on for Dynamics 365 Customer Engagement | MicrosoftDocs"
description: "Configure and enable Sales insights add-on"
keywords: "sales insights addon, insights addon, relationship analytics, predective lead scoring, lead scoring"
ms.date: 05/08/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 93676b52-d168-497d-957f-ae2c8627645a
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 1
topic-status: Drafting
---

# Preview feature: Enable and configure Dynamics 365 AI for Sales

Applies to Dynamics 365 (online), version 9.0.2

Enabling and configuring the Dynamics 365 AI for Sales features helps the user to effectively use the Dynamics 365 AI for Sales app. The Dynamics 365 AI for Sales contains the following features:
- Relationship analytics
- Predictive lead scoring
- Predictive oppportunity scoring
- Notes analysis
- Connection insights

## GDPR
To know about Dynamics 365 AI for Sales related **General Data Protection Regulation (GDPR)**, see [Embedded Intelligence and GDPR](embedded-intelligence-gdpr.md).<br>

## Prerequisites
Review the following requirements before you emable and configure Dynamics 365 AI for Sales feature:
- You must be a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] administrator.
- You must enable **Embedded intelligence**. (../includes/proc-more-information.md)] [How to enable embedded intelligence](configure-enable-embedded-intelligence.md#how-to-enable-embedded-intelligence)

## Enable Dynamics 365 AI for Sales features
Dynamics 365 AI for Sales features are not available by default. You must enable these features by selecting an organization.
Follow these steps:
1. On the **AI setup** page, select **Get it now**.   
    ![Get Dynamics 365 AI for sales](media/d365-ai-sales-getitnow.png "Get Dynamics 365 AI for sales")<br>
2. On the **Sales Insights** installation page, carefully read and select the terms and conditions, and then select **Continue**. <br>
    The installation takes a few minutes to complete, and then the status appears in the status bar.<br>
    ![Accept sales insights addon terms and conditions](media/sales-insights-addon-terms-conditions.png "Accept sales insights addon terms and conditions") <br>
    Status of installation is displayed. When complete, you're ready to configure Dynamics 365 AI for Sales features.

## Configure Relationship analytics
Relationship analytics provides graphical representation of KPIs and activity histories for any contact, opportunity, lead or account. To configure Relationship analytics, follow these steps:

1. On the **Overview** tab, select **Configuration** from **Relationship analytics** section.<br>
   ![Relationship analytics configuration](media/relationship-analytics-configuration.png "Relationship analytics configuration") <br>
-OR-   
You can also select **Relationship analytics** tab. <br>
The configuration page opens.
2. Read and accept the Relationship analytics terms and conditions, and then select **Begin Setup**.
   ![Accept terms and conditions for Relationship analytics](media/relationship-analytics-terms-conditions.png "Accept terms and conditions for Relationship analytics") <br>





## Configure Predective lead scoring




## Configure Predective opportunity scoring



## Configure Notes analysis




## Configure Connection insights



 or **Predective lead scoring** tile, which is on the embedded intelligence **Overview** tab. This option is available only after you install the Sales insights add-on.<br>
![Relationship analytics and Predictive lead scoring configuration](media/relationship-analytics-lead-scoring-configuration.png "Relationship analytics and Predictive lead scoring configuration configuration") <br>

      
   b. On the **Relationship analytics** page, configure the parameters as described in the following table.
      |**Parameter**|**Description**|  
      |---------------------|----------------------------------------------|
      |**Data Sources**|**CRM Activities:** If enabled, all historical data from Dynamics 365 is ingested for computation in Relationship analytics.<br>**Exchange Data:** If enabled, 30 days of data from Exchange is ingested for KPI and health computation. Exchange connector ingests three days of data per day until the last 30 days of data is complete.|  
      |**Relationship Health Score**|Businesses place different emphasis on the type of communication used with customers. You can modify the importance of activities of different types as they contribute to the relationship health score.|  
      |**Communications Frequency**|Businesses have varying sales cycles and different expected levels of communications with customers. A longer expected communications frequency reduces the expectation of more recent frequent communications in the health score. A shorter expected communications frequency increases the expectation of more recent frequent communications in the health score.|<br>
      ![Relationship analytics configuration settings page](media/relationship-analytics-configuration-settings.png "Relationship analytics configuration settings page") <br>
   c. Select **Save**.<br>
      Relationship analytics is configured and ready to use in your organization. <br>
<a name="PredictiveLeadScoring"></a>**Predictive lead scoring:**<br>
   a. On the Predictive lead scoring page, select **Create Model**.<br>
      ![Create model in Predictive lead scoring](media/predictive-lead-scoring-create-model.png "Create model in Predictive lead scoring") <br>
      Creating a model takes few minutes and you can see progress on the screen.<br>
   b. Verify that the **Prediction Accuracy** score from **Model Outcome** matches your organizational requirements and select **Apply Model**.<br>
      ![Predictive lead scoring accuracy score](media/predictive-lead-scoring-score-accuracy.png "Predictive lead scoring accuracy score")
      The prediction lead scoring is applied in your organization and users can see the lead scoring in their views under **Lead Score** column.<br> 
   c. (Optional) If you are not satisfied with the **Prediction Accuracy** score, select **Retrain Model** and apply.<br>
   
    > [!NOTE]
    > We recommend you to train the model once the data is refreshed in our organization for better prediction accuracy scoring.
   
   d. If you want to configure the lead score range, enter minimum value of the range in the Lead Scoring Range.
      When you change lead score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change minimum range value score for **Grade A** to 51, the maximum lead score range for Grade B changes to 50.
      ![Predictive lead scoring change maximun score for grade](media/predictive-lead-scoring-change-max-score.png "Predictive lead scoring change maximun score for grade")
   e. Save and apply the model. <br>
    The predictive lead scoring is configured and ready to use in your organization.

### (Optional) Uninstall the Sales insights add-on

If you don't want to use the Sales insights add-on features for your organization, you can uninstall them. You need to uninstall each feature individual individually. To uninstall these features:
1.	Go to **Settings** > **Customization** > **Solutions**.
    A list of solutions that are installed in your organization is displayed.
2. Select **RelationshipAnalytics**, and then select **Delete**.<br>
   ![Sales insights add-on delete](media/sales-insights-addon-uninstall-ra.png "Sales insights add-on delete") <br>
3. A confirmation message is displayed. Select **OK**.<br>
   The Relation analytics is uninstalled from your organization. 
4. Similarly, repeat step 2 and 3 for **PredictiveLeadScoring** and **SalesInsightsAddOn**.

    > [!NOTE]
    > If you want to install Sales insights add-on in future, makesure that you uninstall the **SalesInsightsAddOn** package too after uninstalling Relationship analytics and Predictive lead scoring.

## Enable Exchange Data   

Enabling Exchange Data allows [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to collect valuable information regarding communications, such as emails and meetings for users in your organization from Exchange. To collect this information, you must provide privileges to connect to exchange server through Admin center.

1.  Go to **Admin** center.    
    ![Admin center](media/sales-insights-addon-admincenter.png "Admin center")

3.  Select **Settings** > **Services & add-ins** > **Dynamics Customer Insights Preview**.
    ![Select customer insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview.png "Select customer insights preview option")

4.  Configure the Dynamics Customer Insights Preview to **on** and select **Save**.<br>
    ![Enable and save customer insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview-settings.png "Enable and save customer insights preview option")

    Now you can connect to exchange server to collect data.

### See also

-  [Get insights on opportunities, activities, and leads of customers](sales-insights-addon.md)
-  [Opt out of relationship analytics (GDPR)](optout-relationship-analytics-gdpr.md)