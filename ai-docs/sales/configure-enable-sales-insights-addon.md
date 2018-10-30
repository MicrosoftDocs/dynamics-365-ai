---
title: "Configure and enable Sales insights add-on for Dynamics 365 Customer Engagement | MicrosoftDocs"
description: "Configure and enable Sales insights add-on"
keywords: "sales insights addon, insights addon, relationship analytics, predictive lead scoring, lead scoring"
ms.date: 10/31/2018
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

# Enable and configure Dynamics 365 AI for Sales capabilities for sellers

Applies to [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] (online), version 9.0.2

Enabling and configuring the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales features helps the user to effectively use the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales. The [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales contains the following features:

- Relationship analytics
- Predictive lead scoring
- Predictive opportunity scoring
- Notes analysis
- Talking points
- Who knows whom

> [!IMPORTANT]
> The AI for Sales features are available only in North American (NAM) regions.

## GDPR

To know about [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales related **General Data Protection Regulation (GDPR)**, see [Dynamics 365 AI for Sales and GDPR](embedded-intelligence-gdpr.md).

## Prerequisites

Review the following requirements before you enable and configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales feature:

- You must purchase **Dynamics 365 AI for Sales** license to use AI sales features.
- You must be a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] administrator.
- Exchange email server is configured, and mailbox is enabled using **Email Configurations** in Settings. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [System Settings dialog box - Email tab](/dynamics365/customer-engagement/admin/system-settings-dialog-box-email-tab).
- If you want to use LinkedIn data for Relationship analytics, verify that LinkedIn solution is installed in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] and write back from LinkedIn Sales navigator is enabled.

## Enable [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales features

[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales features are not available by default. You must enable these features by selecting an organization. Follow these steps:

1. On the **AI setup** page, select **Get it now**.<br>
   ![Get Dynamics 365 AI for sales](media/d365-ai-sales-getitnow.png "Get Dynamics 365 AI for sales")<br>
2. On the **Sales Insights** installation page, carefully read and select the terms and conditions, and then select **Continue**.<br>
   The installation takes a few minutes to complete, and then the status appears in the status bar.<br>
    > [!div class="mx-imgBorder"]
    > ![Accept sales insights addon terms and conditions](media/sales-insights-addon-terms-conditions.png "Accept sales insights addon terms and conditions")
   
    Status of installation is displayed. When complete, you're ready to configure [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales features.
    > [!div class="mx-imgBorder"]
    > ![Dynamics 365 AI for sales is enabled](media/sales-insights-addon-enabled.png "Dynamics 365 AI for sales is enabled")

## Configure Relationship analytics

Relationship analytics provides graphical representation of KPIs and activity histories for any contact, opportunity, lead or account to the users. To configure Relationship analytics, follow these steps:

1. Go to **Settings** > **Setup AI**.<br>
2. On the **Overview** tab, select **Configuration** from **Relationship analytics** section.<br>
    > [!div class="mx-imgBorder"]
    > ![Relationship analytics configuration](media/relationship-analytics-configuration.png "Relationship analytics configuration")

   > [!NOTE]
   > You can also select **Relationship analytics** tab.

   The configuration page opens.
3. Read and accept the Relationship analytics terms and conditions, and then select **Begin Setup**.
    > [!div class="mx-imgBorder"]
    > ![Accept terms and conditions for Relationship analytics](media/relationship-analytics-terms-conditions.png "Accept terms and conditions for Relationship analytics")<br>
4. On the **Relationship analytics** page, configure the parameters as described in the following table.

    |**Parameter**|**Description**|
    |-|-|
    |**Data Sources**|**CRM Activities:** If enabled, all historical data from [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] is ingested for computation in Relationship analytics.<br>**LinkedIn:** If enabled, the data from LinkedIn will be ingested for KPI and health computation. by default, the option is enabled when LinkedIn is installed in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]. Note: This option is not available if LinkedIn is not installed in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)].<br>**Exchange Data:** If enabled, 30 days of data from Exchange is ingested for KPI and health computation. Exchange connector ingests three days of data per day until the last 30 days of data is complete.|
    |**Relationship Health Score**|Businesses place different emphasis on the type of communication used with customers. You can modify the importance of activities of different types as they contribute to the relationship health score.|
    |**Communications Frequency**|Businesses have varying sales cycles and different expected levels of communications with customers. A longer expected communications frequency reduces the expectation of more recent frequent communications in the health score. A shorter expected communications frequency increases the expectation of more recent frequent communications in the health score.|
    > [!div class="mx-imgBorder"]
    > ![Relationship analytics configuration settings page](media/relationship-analytics-configuration-settings.png "Relationship analytics configuration settings page")<br>
5. Select **Save**.<br>
   Relationship analytics is configured and ready to use in your organization.

Enable **Dynamics 365 AI for Sales – Analytics** option in admin center to collect valuable information regarding communications, such as emails and meetings for users in your organization from Exchange server. This data is used in analytics features for salespeople and sales managers. When you enable this, the **Exchange Data** option on relationship analytics configuration page is automatically selected. <br>
To enable Dynamics 365 AI for Sales – Analytics, follow these steps: 

1. Go to **Admin** center.<br>
    ![Admin center](media/sales-insights-addon-admincenter.png "Admin center")<br>

2. Select **Settings** > **Services & add-ins** > **Dynamics 365 AI for Sales – Analytics**.<br>
    ![Select customer insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview.png "Select customer insights preview option")<br>

3. Read the description and configure the Dynamics 365 AI for Sales – Analytics settings as **on** and select **Save**.<br>
    ![Enable and save customer insights preview option](media/sales-insights-addon-admincenter-customer-insights-preview-settings.png "Enable and save customer insights preview option")<br>

    Now you can connect to exchange server to collect data.

> [!NOTE]
> For more information about Relationship analytics and how it can help your users, see [View customer activity history](../sales/relationship-analytics.md)

## Configure Predictive lead scoring

Predictive lead scoring helps users to focus on revenue generation efforts by providing score to prioritize efforts on quality leads. To configure Predictive lead scoring, follow these steps:

1. Go to **Settings** > **Setup AI**.<br>
2. On the **Overview** tab, select **Configuration** from **Predictive lead scoring** section.
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring configuration](media/predictive-lead-scoring-configuration.png "Predictive lead scoring configuration")<br>

   > [!NOTE]
   > You can also select **Predictive lead scoring** tab.

   The configuration page opens.
3. Select **Create Model**.
    > [!div class="mx-imgBorder"]
    > ![Create model in Predictive lead scoring](media/predictive-lead-scoring-create-model.png "Create model in Predictive lead scoring")<br>

   Creating a model takes few minutes and you can see progress on the screen.<br>
1. Verify that the **Prediction Accuracy** score from **Model Outcome** matches your organizational requirements and select **Apply Model**.
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring accuracy score](media/predictive-lead-scoring-score-accuracy.png "Predictive lead scoring accuracy score")<br>
  
    The prediction lead scoring is applied in your organization and users can see the lead scoring in their views under **Lead Score** column.<br>
1. (Optional) If you are not satisfied with the **Prediction Accuracy** score, select **Retrain Model** and apply.<br>
   > [!NOTE]
   > We recommend you to train the model once the data is refreshed in our organization for better prediction accuracy scoring.
1. If you want to configure the lead score range, enter minimum value of the range in the **Lead Scoring Range**.<br>
   When you change lead score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change minimum range value score for **Grade A** to 51, the maximum lead score range for **Grade B** changes to 50.
    > [!div class="mx-imgBorder"]
    > ![Predictive lead scoring change maximum score for grade](media/predictive-lead-scoring-change-max-score.png "Predictive lead scoring change maximum score for grade")<br>
1. Save and apply the model.<br>
   The predictive lead scoring is configured and ready to use in your organization.

> [!NOTE]
> For more information about Predictive lead scoring and how it can help your users, see [Convert leads into opportunities](../sales/work-predictive-lead-scoring.md)

## Configure Predictive opportunity scoring

Predictive opportunity scoring helps users to focus on revenue generation efforts by providing score to prioritize efforts on quality opportunities. To configure Predictive opportunity scoring, follow these steps:

1. Go to **Settings** > **Setup AI**.<br>
1. On the **Overview** tab, select **Configuration** from **Predictive opportunity scoring** section.
    > [!div class="mx-imgBorder"]
    > ![Predictive opportunity scoring configuration](media/predictive-opportunity-scoring-configuration.png "Predictive opportunity scoring configuration")

   > [!NOTE]
   > You can also select **Predictive opportunity scoring** tab.

   The configuration page opens.
1. Select **Create Model**.
    > [!div class="mx-imgBorder"]
    > ![Create model in Predictive opportunity scoring](media/predictive-opportunity-scoring-create-model.png "Create model in Predictive opportunity scoring")

   Creating a model takes few minutes and you can see progress on the screen.<br>
1. Verify that the **Prediction Accuracy** score from **Model Outcome** matches your organizational requirements and select **Apply Model**.
    > [!div class="mx-imgBorder"]
    > ![Predictive opportunity scoring accuracy score](media/predictive-opportunity-scoring-score-accuracy.png "Predictive opportunity scoring accuracy score")<br>
    The prediction opportunity scoring is applied in your organization and users can see the opportunity scoring in their views under **Opportunity Score** column.<br>
1. (Optional) If you are not satisfied with the **Prediction Accuracy** score, select **Retrain Model** and apply.<br>
   > [!NOTE]
   > We recommend you to train the model once the data is refreshed in our organization for better prediction accuracy scoring.
1. If you want to configure the opportunity score range, enter minimum value of the range in the Opportunity Scoring Range.<br>
   When you change opportunity score range for a grade, the preceding grade's maximum range value changes automatically depending on the changed minimum grade value. For example, when you change minimum range value score for **Grade A** to 70, the maximum opportunity score range for **Grade B** changes to 69.<br>
   ![Predictive opportunity scoring change maximun score for grade](media/predictive-opportunity-scoring-change-max-score.png "Predictive opportunity scoring change maximun score for grade")<br>
1. Save and apply the model.<br>
   The predictive opportunity scoring is configured and ready to use in your organization.

> [!NOTE]
> For more information about Predictive opportunity scoring and how it can help your users, see [Convert opportunities into deals](../sales/work-predictive-opportunity-scoring.md)

## Configure Notes analysis

To help users with intelligent auto suggestions when they enter notes regarding a recent meeting or discussion with customer in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], enable Notes analysis.

1. Go to **Settings** > **Setup AI**.<br>
2. After you enable [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] AI for Sales features, select the toggle button to enable **Notes analysis**.
    > [!div class="mx-imgBorder"]
    > ![Enable notes analysis](media/notesanalysis-enable.png "Enable notes analysis")

> [!NOTE]
> For more information about Notes analysis and how it can help your users, see [How Notes analysis assists you with intelligent suggestion](notes-analysis.md)

## Configure Talking points

Talking points feature is available under Connection insights configuration page. This feature help users in your organization to quickly establish communications with customers.

1. Go to **Settings** > **Setup AI**.<br>
2. On the **Overview** tab, select **Configuration** from **Connection insights** section.
    > [!div class="mx-imgBorder"]
    > ![Connection insights configuration](media/connection-insights-configuration.png "Connection insights configuration")

   > [!NOTE]
   > You can also select **Connection insights** tab.
  
   The configuration page opens. 
3. On the **Talking points** section, select **Turn on Talking points for your organization**.<br>
    The categories are automatically selected.<br>
    > [!div class="mx-imgBorder"]
    > ![Enable talking points](media/talkingpoints-enable.png "Enable talking points")
        
    > [!NOTE]
    > You can select only the categories that meets your organizational requirements.
4. Select **Save**.<br>
    The Talking points is configured and ready to use in your organization.
    
> [!NOTE]
> For more information about Talking points, see [Know conversation starters for your customers](../sales/talking-points.md)

## Configure Who knows whom

Who knows whom feature is available under Connection insights configuration page. This feature help users to quickly identify colleagues within their organization who can introduce them to leads or contacts.

1. Go to **Settings** > **Setup AI**.<br>
2. On the **Overview** tab, select **Configuration** from **Connection insights** section.
    > [!div class="mx-imgBorder"]
    > ![Connection insights configuration](media/connection-insights-configuration.png "Connection insights configuration")

   > [!NOTE]
   > You can also select **Connection insights** tab.
  
   The configuration page opens.
3. On the **Who knows whom** section, select **Turn on Who Knows Whom for your organization**.<br>
    > [!div class="mx-imgBorder"]
    > ![Enable who knows whom](media/who-knows-whom-enable.png "Enable who knows whom")
        
4. Optionally, you can select the **Email template** according to your organizational requirements. By default, an out-of-the-box email template will be selected.
5. Select **Save**.<br>
   The Who Knows Whom is configured and ready to use in your organization.<br>

After you enable the Who knows whom feature in your organization, verify that the connection graph is enabled in the admin center. This allows the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to collect the communication and collaboration details of users from exchange server.<br>
> [!NOTE]
> Contact your Office 365 administrator to enable Dynamics 365 AI for Sales connection graph if you do not have sufficient privileges to enable. 
 
To configure Dynamics 365 AI for Sales connection graph, follow these steps:<br>

1. Go to **Admin** center.<br>
    ![Admin center](media/sales-insights-addon-admincenter.png "Admin center")<br>
2. Select **Settings** > **Services & add-ins** > **Dynamics 365 AI for Sales – Connection Graph**.<br>
    ![Select connection graph option](media/sales-insights-addon-admincenter-connection-graph-option.png "Select connection graph option")<br>
3. Read the description and configure the Dynamics 365 AI for Sales – Connection Graph settings as **on**.<br>
    ![Enable and save connection graph](media/sales-insights-addon-admincenter-connection-graph-enable.png "Enable and save connection graph")<br>
4. (Optional) If you do not want to collect information on any group of users in your organization, add the group ID in the text box.<br> 
    ![Enable and save connection graph](media/sales-insights-addon-admincenter-connection-graph-exclude-group.png "Enable and save connection graph")<br>
5. Select **Save**.

> [!NOTE]
> For more information about Who knows whom, see [Get introduced to lead](../sales/who-knows-whom.md)
<!--
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
-->

## Privacy notice  

For specific privacy information about Dynamics 365 AI for Sales capabilities for sellers, see [Privacy notice](privacy-notice-seller.md).

### See also

- [Opt out of relationship analytics (GDPR)](optout-relationship-analytics-gdpr.md)
- [GDPR for Sales insights add-on](embedded-intelligence-gdpr.md)
- [View and export KPI data (GDPR)](view-export-KPI-data-gdpr.md)
- [Retrieve insights data using msdyn_RetrieveTypeValuesFromDCI action](retrieve-insights-data-msdyn-RetrieveTypeValuesFromDCI.md)