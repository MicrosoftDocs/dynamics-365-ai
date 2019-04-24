---
title: "Licensing and capacity overview"
description: "Details on the licensing structure for Customer Service Insights."
keywords: ""
ms\.date: 4/24/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: tpalmer
ms.author: tpalmer
manager: shellyha
---

# Licensing and capacity overview

Your organization can obtain separate licenses for Dynamics 365 Customer Service Insights, or licensing may be included with another Microsoft service offering. For example, Dynamics 365 for Customer Service includes entitlements for Customer Service Insights. As with most Microsoft licensing, you can mix and match so it works for your users.

All licenses for Customer Service Insights are user-based. In the rest of this article we will highlight some of the key points of licensing. However, you should consult the [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544) for the latest details. 

A Customer Service Insights license comes with a limit on the number of cases that can be imported. Today, that limit is 100k cases/user/month. 

## Case Capacity

The required case capacity is determined by the total number of case records imported into Customer Service Insights workspaces. The number of cases imported into a workspace is the number of cases created in a 60 day window to which the workspace owner has read access. Note that if multiple workspaces are connected to the same Dynamics 365 environment, the same records may be imported multiple times and each import will count towards the total capacity.

If you require additional case capacity, you can include the optional capacity add-on licenses with your subscription. Subscription add-ons apply across a single tenant; they are not tied to a specific user. 

## Example license calculations

As described above, the required case capacity can be calculated using multiple parameters. 

a) Average cases created in last 60 days in the Dynamics environment*  
b) The number of cases owner has read access to out (may be a subset of a)  
c) The number of Customer Service Insights workspaces connected to a CDS environment (sample workspace is not counted)  

| (a) <br> Average cases created in last 60 days* in the Dynamics environment	| (b) <br> # cases owner has read access to out of the # in a)	| (c) <br> # Customer Service Insights workspaces	| <br> Minimum required case capacity (b*c)|
|--|--|--|--|
|200k	|100k	|1	|100,000|
|200k	|200k	|1	|200,000|
|200k	|200k	|2	|400,000|
|600k	|300k	|1	|300,000|
|600k	|600k	|1	|600,000|
|600k	|600k	|2	|1,200,000|



*Whether or not a case was created in the last 60 days is determined by the [mapping of the "Created On" source field in Customer Service Insights](map-data.md).    
If no custom mapping is in place, it's the [createdOn field in the Case entity](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/service/case#createdOn).
