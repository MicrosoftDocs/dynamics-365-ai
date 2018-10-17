---
title: "Set up Market Insights | Microsoft Docs"
description: "Learn how you can set up Market Insights in a few steps."
keywords: "configuration, setup, quickstart, reference"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 13cb8bad-86fa-4be2-b60c-0c00e329f31f
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

# Set up [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)]
This topic explains what the Administrator for your organization does to set up [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)].  
  
<a name="set_sol_default"></a>   
## Define global settings  
 You need to set up [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)] so your users can work with [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] data. Begin by setting the system defaults. [!INCLUDE[proc_permissions_social_listening_admin](../includes/proc-permissions-admin.md)]  
  
1.  Go to **Settings** > **Global Settings**.  
  
2.  In the list, click **Default Preferences**.  
  
3.  In the **Default Preferences** pane, set your options.  
  
    |Option|What you can do|  
    |------------|---------------------|  
    |Name|Edit the name of your solution.|  
    |Screen language|Set the default language for the user interface.|  
    |Default time frame|Define the default time frame for your users’ analysis.|  
    |Date and time format|Set the default date and time format. To edit the current values, click **Edit**.|  
    |Number format|Select the number format from a predefined set of options to show numbers on the user interface.|  
  
4.  Click **Save**.  
  
> [!NOTE]
>  The default values apply to all users for your organization. However, users can override the default settings for their accounts by editing them in **Settings** > **Personal Settings** > **Your Preferences**.  
  
<a name="set_up_first"></a>   
## Set up your first search topic and add rules  
 After you set up your system defaults, define your first search topic so you have data available to analyze. Think about what topics are relevant to your users. The number of rules for a topic isn’t limited, and you can edit your rules anytime.  
  
1.  Go to **Search Setup**.  
  
2.  In the **Search Topics** pane, click the **Add** button ![add button](media/add-icon.png "Add button").  
  
3.  Name your search topic and assign a category.  
  
4.  Under **Rules**, click the **Add rule** button ![add button](media/add-icon.png "Add button").  
  
5.  Select the rule type that you want to add, and configure the rule.  
  
6.  In the rule pane, click **Continue** to see an approximate number of posts that you can expect from this rule. If the rule is within your post quota, you’ll be allowed to save it. Otherwise, a message will appear and indicate that you exceeded the quota.  
  
7.  Repeat steps 4 through 6 until you have added all required rules for this search topic. (Optional)  
  
8.  In the **Search Topic Settings** area, click **Save** ![save button](media/save-icon.png "Save button") to save the search topic and start data acquisition.  
  
> [!NOTE]
>  You can create an unlimited number of search topics to meet your requirements for [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)]. However, make sure that you stay within your post quota to keep data acquisition up and running.  More information: [Set up searches to listen to social media conversations](set-up-searches.md)  
  
### Privacy notices  
 [!INCLUDE[cc_privacy_msl_social_services_content](../includes/cc-privacy-market-insights-social-services-content.md)]  
  
 [!INCLUDE[cc_privacy_msl_index_cached_data](../includes/cc-privacy-market-insights-index-cached-data.md)]  
  
### See Also  
 [Administer Market Insights](settings-administration.md)   
 [Manage global settings](manage-global-settings.md)   
 [Set up searches to listen to social media conversations](set-up-searches.md)   
 [Assign permissions and user roles](assign-user-roles.md)
 
