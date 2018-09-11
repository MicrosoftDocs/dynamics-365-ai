---
title: "Link posts from Social Engagement to Dynamics 365 | Microsoft Docs"
description: "Learn how to link social posts to Dynamics 365 and create new case or lead records."
keywords: "link to crm, link to customer engagement"
ms.date: 03/16/2018
ms.service: dynamics-365-marketing
ms.topic: article
applies_to: 
  - "Social Engagement"
ms.assetid: e97a38d7-37c4-4dce-b02e-1076ad992cff
author: m-hartmann
ms.author: mhart
manager: sakudes
topic-status: Drafting
ms.custom: 
  - dyn365-socialengagement
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Link posts from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to Dynamics 365

[!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)] provides a platform for capturing public posts from social media. You link posts in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance and turn them into new records in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].

When you link a post from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] instance, a Social Activity record is created in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]. [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] can turn these social activities into other types of [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records, for example into a lead, an opportunity, or a case.
  
## Steps for linking posts from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to Dynamics 365  

1. First, [set up the feature to link social posts](connect-dynamics-365-record-creation.md) to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance as social activities. As a [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] Administrator, you need to connect [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] with [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].   
  
2. Next, you can [define the attributes](create-dynamics-365-record-from-social-post.md) for the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] entities that you want to display in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].   
  
3. As a system administrator or customizer in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)], you can configure rules to handle newly created social activities by using the [**Automatic Record Creation and Update Rules**](configure-automatic-record-creation.md) feature in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)].   
  
4. When everything is set up, your users can start to link social posts to create or update [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records.   
   [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Create a new Dynamics 365 record from a social post](create-dynamics-365-record-from-social-post.md)  
  
5. Optionally, you can configure [automation rules](automation-rules.md) in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to create new [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records for posts that match a specified data set.   
  
6. Understand how to [delete or disable a connection](manage-connection-dynamics-365-record-creation.md) between [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] and [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)], and understand how this might affect existing linkages or linking newly acquired social posts.   
  
### Privacy notice 
 
 [!INCLUDE[cc_privacy_mse_post_and_automation_rules](../includes/cc-privacy-mse-post-and-automation-rules.md)]  
  
### See also  

 [Administer Market Insights](settings-administration.md)   
 [Set up the connection between Dynamics 365 and Market Insights](connect-dynamics-365-record-creation.md)   
 [Create a new Dynamics 365 record from a social post](create-dynamics-365-record-from-social-post.md)
