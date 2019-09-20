---
title: " Dynamics 365 Sales Insights capabilities Privacy Notices | Microsoft Docs"
description: "Privacy notices Sales Insights capabilities."
keywords: "privacy notice, privacy statement addition"
ms.date: 10/01/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 40143ca0-2e09-4fb0-9c80-406671024000
author: udaykirang
ms.author: udag
manager: shujoshi
ms.custom: dyn365-ai-sales
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---


# Sales Insights privacy notice 

Your privacy is important to us. For Microsoft Online Services, read the [Microsoft Online Services privacy Statement](https://go.microsoft.com/fwlink/p/?LinkID=389041).

## Sales Insights free features

For specific privacy information about Sales insights free features, refer to the paragraphs below.

[!INCLUDE[cc_privacy_relationship_insights_relationship_assistant](../includes/cc-privacy-relationship-insights-relationship-assistant.md)]

[!INCLUDE[cc_privacy_relationship_insights_email_engagement](../includes/cc-privacy-relationship-insights-email-engagement.md)]

[!INCLUDE[cc_privacy_relationship_insights_auto_capture](../includes/cc-privacy-relationship-insights-auto-capture.md)]

## Sales Insights advanced features

For specific privacy information about Dynamics 365 Sales Insights advanced features, refer to the paragraphs below.

By enabling [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] capabilities, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Data will be sent to and used by (1) Azure Data Factory for the purpose of data movement and transformation for KPI computation, and (2) Azure Container Instance for the purpose of predictive model training and scoring. By installing this solution, you agree for this limited set of data to be sent to Azure Data Factory service and Azure Container Instance.

Azure components and services that are involved with Dynamics 365 Sales Insights are detailed in the following sections.
[!Include[cc_privacy_note_azure_trust_center](../includes/cc-privacy-note-azure-trust-center.md)]

### Azure Data Factory
[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] uses Azure Data Factory, a cloud data integration service, to orchestrate and automate the movement and transformation of data (including Customer Data) between services.

### Azure Container Instance
[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] uses Azure Container instance, a cloud-based container service, to create predictive model training and scoring pipelines dynamically. 

### Installation and Removal of Dynamics 365 Sales Insights

An administrator can enable [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] capabilities by installing it as a solution in the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization. In addition, an administrator can subsequently disable the feature by uninstalling this solution from the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] organization.

## Sales Insights application

For specific privacy information about [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] application, refer to the paragraphs below.

By enabling [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] Preview capabilities, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Data, (1) Azure Data Factory for the purpose of data movement and transformation for KPI computation and (2) will be sent to Bing news to acquire relevant and up to date news on products, industries and customers.>

By installing this solution, you agree for this limited set of data to be sent to Azure Data Factory and the Bing service.

By setting up the Conversation Intelligence feature, Customer Data will be sent to and used by (1) Azure Event Grid for the purpose of identifying when new call recording files are available for media processing.

### Azure Services

Azure components and services that are involved with [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] Preview are detailed in the following sections.

[!Include[cc_privacy_note_azure_trust_center](../includes/cc-privacy-note-azure-trust-center.md)]

### Azure Data Factory

[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] Preview uses Azure Data Factory, a cloud data integration service, to orchestrate and automate the movement and transformation of data (including Customer Data) between services.

### Azure Event Grid

[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] Preview (Conversation intelligence) uses Azure Event Grid, a cloud event handling service, to receive events when new call recording files are added to the customer’s blob storage for processing, and when Azure Media Service completes processing the media files.  

The data passed in these events include Azure storage account name, blob container name and call recording filename.

### Other services

#### Bing 

[!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] Preview insight app uses Customer Data from the name, address, and industry fields of your account records and sends it to Bing (a consumer service) for the purpose of showing relevant news. Data sent to Bing will be devoid of any of your company’s information and only stored for diagnostics purposes. 

### Installation and removal of the Sales Insight preview app

[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] users and administrators who are allowed to register new applications in Azure Active Directory, can enable the Sales Insight preview app by signing in to the app and consenting to the required permissions. Administrators can change these permissions, which can include removing access to the app, at https://myapps.microsoft.com 

### Handling GDPR for conversation intelligence

It is the enterprise customer’s responsibility to comply with the GDPR. If you choose to honor and execute a data subject rights (DSR) request for delete or edit, please email [Microsoft](mailto:D365callintelligence@microsoft.com) and Microsoft will manually process the DSR to delete and edit.


### See also

[Introduction to administer Sales Insights](../sales/intro-admin-guide-sales-insights.md)