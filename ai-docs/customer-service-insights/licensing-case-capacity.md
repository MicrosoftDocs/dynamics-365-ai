---
title: "Licensing and case capacity considerations"
description: "Key points about licensing and case capacity determinations for Dynamics 365 Customer Service Insights."
keywords: ""
ms\.date: 4/25/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: tpalmer
ms.author: tpalmer
manager: shellyha
---

# Licensing and case capacity considerations

<!--note from editor: Suggest hyphenating "case capacity" when it's an adjective, but I did not do this due to the number of headings that phrase is in; did not want to break links.   -->

Your organization can obtain separate licenses for Dynamics 365 Customer Service Insights, or licensing might be included with another Microsoft service offering. For example, Dynamics 365 for Customer Service includes entitlements for Customer Service Insights. All licenses for Customer Service Insights are user based. As with most Microsoft licensing, you can mix and match to meet the needs of your users.

This article highlights some key points that are important to know about licensing and case capacity determinations for Customer Service Insights. However, you should consult the [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544) for the latest details. 

## Case capacity add-on licensing
A Customer Service Insights license comes with a limit on the number of cases that can be imported. Today, that limit is 100,000 cases per user per month (cases/user/month). 

Case capacity is determined by the total number of case records imported into Customer Service Insights workspaces. The number of cases imported into a workspace is defined as the number of cases created in a 60-day period to which the workspace owner has read access. Note that if multiple workspaces are connected to the same Dynamics 365 environment, the same records can be imported multiple times, and each import counts towards the total case capacity.

If you require additional case capacity, you can include optional capacity add-on licenses with your subscription. Subscription add-ons apply across a single organization; add-ons are not tied to a specific user. 

## Calculating required case capacity for licensing purposes

The required case capacity for an organization can be determined based on multiple factors: 

- Average number of cases created in the last 60 days in an organization's Dynamics 365 environment* (**A**)  
- Number of cases an owner has read access to, which might be a subset of the average number of cases created in the last 60 days (**B**)  
- Number of Customer Service Insights workspaces connected to a Common Data Service environment, excluding the sample workspace (**C**)  

| Average cases created in the last 60 days in the Dynamics 365 environment* (A)	| Number of cases owner has read access to out of the average (B)	| Number of Customer Service Insights workspaces (C)	| Minimum required case capacity (multiply B and C)|
|--|--|--|--|
|200,000	|100,000	|1	|100,000|
|200,000	|200,000	|1	|200,000|
|200,000	|200,000	|2	|400,000|
|600,000	|300,000	|1	|300,000|
|600,000	|600,000	|1	|600,000|
|600,000	|600,000	|2	|1,200,000|


*Whether a case was created in the last 60 days is determined by the [mapping of the "Created On" source field in Customer Service Insights](map-data.md). If no custom mapping is in place, it is determined by the [createdOn field in the case entity](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/service/case#createdOn).


