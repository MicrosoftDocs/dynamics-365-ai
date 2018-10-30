---
title: " [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] capabilities for sales managers Privacy Notices | Microsoft Docs"
description: "Privacy notices for AI for Sales capabilities for sales managers."
keywords: "privacy notice, privacy statement addition"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: cc68a9f0-b3ee-4d4c-87e7-10c1bc111226
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

# [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] capabilities for sellers Privacy Notices

Your privacy is important to us. For Microsoft Online Services, read the [Microsoft Online Services privacy Statement](https://go.microsoft.com/fwlink/p/?LinkID=389041).

For specific privacy information about [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] capabilities for sellers, refer to the paragraphs below.

By enabling [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] Preview capabilities, [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Data, (1) Azure Data Factory for the purpose of data movement and transformation for KPI computation and (2) will be sent to Bing news to acquire relevant and up to date news on products, industries and customers.  
By installing this solution, you agree for this limited set of data to be sent to Azure Data Factory and the Bing service.
By setting up the Call Intelligence feature, Customer Data will be sent to and used by (1) Azure Event Grid for the purpose of identifying when new call recording files are available for media processing.

## Azure Services

Azure components and services that are involved with [!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] Preview are detailed in the following sections.

[!Include[cc_privacy_note_azure_trust_center](../includes/cc-privacy-note-azure-trust-center.md)]

## Azure Data Factory

[!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] Preview uses Azure Data Factory, a cloud data integration service, to orchestrate and automate the movement and transformation of data (including Customer Data) between services.

## Azure Event Grid
[!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] Preview (Call intelligence) uses Azure Event Grid, a cloud event handling service, to receive events when new call recording files are added to the customer’s blob storage for processing, and when Azure Media Service completes processing the media files.  
The data passed in these events include Azure storage account name, blob container name and call recording filename.

## Other services

### Bing 
[!INCLUDE[pn_dynamics_ai_sales](../includes/pn-dynamics-ai-sales.md)] Preview insight app uses Customer Data from the name, address, and industry fields of your account records and sends it to Bing (a consumer service) for the purpose of showing relevant news. Data sent to Bing will be devoid of any of your company’s information and only stored for diagnostics purposes. 

## Installation and removal of the AI for Sales Preview insight app
[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] users and administrators who are allowed to register new applications in Azure Active Directory, can enable the AI for Sales Preview insight app by signing in to the app and consenting to the required permissions. Administrators can change these permissions, which can include removing access to the app, at https://myapps.microsoft.com 

## Handling GDPR for call intelligence
It is the enterprise customer’s responsibility to comply with the GDPR.  If you choose to honor and execute a data subject rights (DSR) request for delete or edit, please email [Microsoft](mailto:D365callintelligence@microsoft.com) and Microsoft will manually process the DSR to delete and edit.


### See also

- [View overall sales insights](../sales/d365-ai-overview.md)
- [Analyze team performance](../sales/d365-ai-team-performance.md)
- [Analyze business performance](../sales/d365-ai-business-performance.md)
- [Analyze customer calls](../sales/call-intelligence.md)