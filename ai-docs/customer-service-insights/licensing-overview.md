---
title: "Licensing Overview"
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

# Licensing Overview

[!INCLUDE [public-preview](../includes/public-preview.md)]

Organizations can obtain licenses by either licensing for Dynamics 365 Customer Service Insights or by it being included in the license of another Microsoft cloud service offering. For example, Dynamics 365 for Customer Service provide entitlements for Dynamics 365 Customer Service Insights. As with most Microsoft licensing, you can mix and match for users as appropriate giving some additional entitlements.

Regardless of how they are obtained all licenses are user based. In the rest of this section we will highlight some of the key points of licensing, but you should consult the Dynamics licensing guide for any of the latest details. 

A Dynamics 365 Customer Service Insights license comes with a limit on the number of cases that can be imported. Today that limit is 100k cases/user/month. 

## Case Capacity

The required case capacity is determined by the total number of case records imported into Customer Service Insights workspaces. The number of cases imported into a workspace is the number of cases created in a 60 day window to which the workspace owner has read access. Note that if multiple workspaces are connected to the same Dynamics environment, the same records may be imported multiple times and each import will count towards the total tenant capacity. See below for some examples. 

If you require additional cases capacity, you can include the optional add-on licenses with your subscription. Subscription add-ons apply across a single tenant; they are not tied to a specific user. 

Default Capacity: 100K cases/user/month 

Capacity Add-on: 500K cases/tenant/month 

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



*Whether or not a case was created in the last 60 days is determined by the source field the "Created On" field is [mapped to](https://docs.microsoft.com/dynamics365/ai/customer-service-insights/map-data). By default (i.e. no custom mapping) this would be the ["createdOn" field](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/service/case#createdOn) in the Case entity.