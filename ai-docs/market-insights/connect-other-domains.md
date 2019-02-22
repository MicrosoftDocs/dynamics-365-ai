---
title: "Allow requests from other domains with Market Insights | Microsoft Docs"
description: "Learn how to add URLs to the list of allowed domains so they can request data from Market Insights."
keywords: allowed domains, connection, integration
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 1f110312-f6fb-4b1d-bdb0-80c37e65acbc
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---
# Connect [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to other domains

(This topic is pre-release documentation and is subject to change.)

Enable communication between [!INCLUDE[Dynamics 365 Market Insights](../includes/pn-market-insights-long.md)] and other compatible applications (such as [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)]) by adding domains that are allowed to make requests for your [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] data to a list. You can remove domains from the list to disallow communications.

To add or remove domains, or to connect [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to another application, you must be a [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] Administrator.

You can enter the following values in your list of allowed domains:  
  
- Full domain names: This enables communication between the specified domain and your [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] solution, for example, `app.contoso.com`  
  
- Domain names with wildcards: This enables communication between all subdomains of the entered domain and your [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] solution, for example, `*.contoso.com`  
  
- Host names: This enables communication between a custom host name and your [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] solution, for example, `http://hostname`  

> [!IMPORTANT]
> Make sure to remove trailing slashes from the domain name.

## Add a domain
  
1.  Go to **Settings** > **Connections** > **Allowed Domains**.  
  
2.  Type the domain name in the input field, and then click the **Add** button ![new or add button](media/plus-icon.png "New or Add button").  
  
## Remove a domain  
  
1.  Go to **Settings** > **Connections** >**Allowed Domains**.  
  
2.  Locate the domain you want to remove, click the **Delete** button ![delete button](media/delete-icon.png "Delete button"), and then confirm the deletion.  
  
## Add the solution URL to the configuration page

In the **Solution URL** pane of the **Allowed Domains** page, you’ll find the **URL** to connect to this instance of [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].  
  
Copy the solution URL and paste it into the configuration page of the application that you want to connect to [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].  
  
> [!NOTE]
> Make sure to add the domain or host name of the application you plan to connect to [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to your list of allowed domains.  
> 
>  To make sure only the domains you own can make requests to your data, we recommend you add your organization’s domain to the list of allowed domains. When a specific domain is added to the list of allowed domains, *.dynamics.com is automatically removed from the allowed domains.  
  
### See Also

[Administer Market Insights](settings-administration.md)   
[Get started with Market Insights](get-started.md)   
