---
title: "Adaptive learning in Market Insights | Microsoft Docs"
description: "Sentiment analysis and the organization-based machine learning models which learn from your inputs."
keywords: "adaptive learning, sentiment analysis, machine learning, ai, intelligence"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: d7ec0e2f-1664-49cf-9759-2d610692a1d0
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

# Adaptive learning based on changes to organization’s sentiment values

[This topic is pre-release documentation and is subject to change.]

[!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)] uses *adaptive learning* to gain information about your edits and confirmations on sentiment values. With adaptive learning, every edit on the sentiment value of posts contributes to the way that sentiments are determined for your organization.  
  
To manage adaptive learning, you need to be a [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] Administrator. However, every user can edit the sentiment value of a post. 
  
> [!NOTE]
>  Edited and confirmed sentiment values only apply to your organization database. Edits and confirmations performed on other organizations’ databases have no impact on how the sentiment is determined for your organization.  
  
## Activate or deactivate machine learning for your organization
  
By default, machine learning is active for your organization, but you can turn it off at any time.  
  
1.  Navigate to **Settings** > **Global Settings**.  
  
2.  In the list, click **Sentiment**.  
  
3.  On the **Sentiment** pane, clear the **Adaptive learning** check box.  
  
4.  Click **Save** ![save button](media/save-icon.png "Save button").  
  
Your organization’s sentiment analysis no longer learns from your users’ edits.  
  
To turn machine learning on, select the **Adaptive learning** check box and click **Save** ![save button](media/save-icon.png "Save button").   

## Reset your organization’s sentiment analysis  

When comparing several months of sentiment data, consider the matured sentiment calculation over time. If you aren’t happy with the results of the adaptive learning model, you can always reset your organization’s sentiment analysis to the system default. This will discard all previously made edits and confirmations to sentiment values, and restart the learning from the system default. You’ll find the date of the restart at the bottom of the page when you go to **Global Settings** > **Sentiment**.  
  
1.  Navigate to **Settings** > **Global Settings**.  
  
2.  In the list, click **Sentiment**.  
  
3.  On the **Sentiment** pane, click **Reset**.  
  
> [!CAUTION]
>  There’s no way of undoing this reset. Use this functionality careful to avoid accidental loss of all your users’ edits and confirmation to sentiment values.  
  
### See Also  
[Manage global settings](manage-global-settings.md)   
[Understand the public perception using sentiment analysis](analytics-sentiment.md)