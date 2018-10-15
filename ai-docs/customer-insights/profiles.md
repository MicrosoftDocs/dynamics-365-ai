---
title: "Profiles | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/31/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
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
robots: noindex,nofollow
---
# Profile

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

This page serves as the best source of insights around each of your customers. 
- The top row lists some of your **Top Paying Customers**.
- The second row present some of your **Most Engaged Customers**. 
- The third row show some of your customers that have the **Most Active Cases**.
- The last row includes a sample of your total customer base.

Each of your customers is represented by a **Customer Card** tile. This card includes:
- The customer's **name, city, gender, marital status and job title** - all taken from the customer's account profile.  
- The Customer's **contact details** including phone number and email address. Those are clickable and will take you to the chosen method of communication.
- The customer's **engagement score:** How engaged is the specific customer compared to other customers? Dynamics 365 AI for Customer Insights uses one of the standard methodologies for calculating engagement score. As part of this methodology, all the customer activities are taken into consideration, weighted according to their types, recencies and frequencies, and normalized on a 1-100 scale. 
- The customer's **lifetime spend:** How much has the customer spent over the course of their engagement with the business. Customer lifetime spend is one of the most comprehensive and actonable indicators of a business health and it combines both sales and deals in process.
- The number of **active cases** and **active segments** for that customer (see Segmentation for an explanation of active segments).  

> [!div class="mx-imgBorder"] 
> ![](media/customer-profiles75.png "Generated customer profiles")

Select **See all** to see more customers sorted by the profile type. In this example, **Top paying** is the profile type.

> [!div class="mx-imgBorder"] 
> ![](media/view-more-customers.png "View more customers")

You can use the customer profiles page to filter and sort the profiles.

> [!div class="mx-imgBorder"] 
> ![](media/filter-sort.png "Filter and sort customer profiles")

What's in the sort list depends on the category you selected earlier and the profile type. 

> [!div class="mx-imgBorder"] 
> ![](media/sort-list.png "Sort list")

Upon clicking a specific customer tile, you will get to the **Power BI report** for that customer.
