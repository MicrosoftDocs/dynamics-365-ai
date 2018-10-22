---
title: "Manage the post quota for Market Insights | Microsoft Docs"
description: "Learn how you can get the most out of your Market Insights post quota."
keywords: "quota, post quota, contingent"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 8eeba9fd-f9f7-4ba4-bf06-43ba71e3333e
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

# Manage your post quota
Keep track of the number of posts that result from your search topics and count toward your solution's post quota. Your solution is priced based on the number of posts you can acquire per month.  
  
If you're expected to exceed the post quota for the current month, administrators get a notification email. When you exceed your post quota, data acquisition will be stopped for either of the following reasons:  
- You still exceed your post quota after a grace period of 48 hours from the time the notification was sent.  
- Your solution passes the additional post quota granted for the grace period, which is five times your monthly allocated quota.

For example, if your monthly post quota is 10,000 posts, your grace period starts when you receive a notification that your solution will probably exceed your quota limits. Data acquisition will be stopped automatically after 48 hours if you have exceeded your post quota by then, or as soon as your solution gathered more than 50,000 posts before the 48 hours have passed. 
  
You have the following options to take action:  
- Review your search topics regularly to make sure that only relevant data is selected. Previewing a search topic before saving it is a great help to get an impression of how many posts we're expecting for the configuration you provided. [Delete search topics or rules](create-delete-search-topic.md) that you don't need anymore. 
- [Maintain a list of blocked content](search-results-quality.md) to avoid any posts appearing in your results from the domains in the list or matching any blocked keywords.  
- [Exclude authors](manage-authors.md) who publish irrelevant posts that match one of your search queries.  
  
> [!CAUTION]
>  Proceed carefully when excluding an author or blocking contents. Posts matching items on the list of blocked contents will be deleted irreversibly after four hours.    

  
## Get the post quota status  
To get a quick overview of the post quota for all your search topics, for single categories or for single search topics, go to **Search Setup** > **Summary**. For more detailed quota information, drill down into the categories and search topics to see the quota usage of these items.  

|       Quota status       |                                                                           Appears                                                                           |                                                                                      What you should do                                                                                      |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|       Within quota       |                                           When the calculated expectations are still within your monthly limits.                                            |                                                                                    No action is required.                                                                                    |
| Expected to exceed quota |                                   If your solution is expected to reach your monthly quota before the current month ends.                                   |            Monitor your post quota closely. Alternatively, increase the post quota, or edit or remove search topics or [!INCLUDE[tn_facebook](../includes/tn-facebook.md)] pages.            |
|      Quota exceeded      |                                              If your solution acquired more posts than your post quota allows.                                              | Take immediate action by adding post quota. Your solution will continue to acquire posts until you either surpass the granted grace period or you reach the additionally granted post quota. |
|   Acquisition stopped    | When Administrators were informed and the solution exceeded your post quota without any action taken. The solution's acquisition was stopped automatically. |                          Increase the post quota to restart your acquisition immediately, or wait until the first day of the next month to restart the acquisition.                          |
  

  
## Keep the post quota healthy  
 Keeping the post quota healthy is crucial to make sure data acquisition isn't interrupted and you don't miss any relevant information.  
  

### Impact of exceeding limits  
 All [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)] administrators receive email notifications about the monthly post quota. To reduce the number of posts found by your solution, you can narrow your search topics by removing rules that you don’t need any more. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Manage the quality of your search results](search-results-quality.md)  
  
 If no action is taken, exceeding the post quota will get your solution blocked from data acquisition until the end of the month. No more posts are acquired, even if they match your search topics.  

> [!IMPORTANT]
>  Note that [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] doesn't gather posts retroactively. Any post that you missed won't appear in your solution if you update your post quota after the acquisition has stopped.  
  
### Understand estimations  
 On the **Summary** page in the **Search Setup** area, you'll find quota information for all active search topics. The following values are provided for each search topic and all categories that contain a search topic:  
  
- **Monthly post quota**: The initial amount of posts that can be acquired each month.  
  
- **Current number of posts:** The total number of posts (including hidden and visible posts) that were acquired during the current calendar month.  
  
- **Expected number of posts:** The calculated number of posts that [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] is expecting until the end of the calendar month, based on the number of current posts.  
  
When you set up a search topic, you can validate the rules to estimate how their volume affects your post quota. The rule validation provides the number of posts that would match your query within a month, based on the post volume of the past month.  

We'll warn you before saving a search topic if we expect more posts than your monthly post quota. You can't save a search topic if the estimations exceed five times the monthly post quota.

Additionally, if you have [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] selected as a source, you'll find a preview of the most recent tweets matching your keywords rule.  
  
> [!CAUTION]
>  Peaks and trending terms can't be estimated. For example, if you set up a search topic in advance for a conference that you plan to establish a hashtag for, the estimates can be far off. Be aware that the post volume will rise significantly when the conference starts, which will affect your post quota. Deleting a search topic will stop the acquisition of posts for this topic, but will not recover your quota&mdash;meaning you will see no difference in the number of current posts. If you want to recover your quota, you will have to add the keywords of a deleted topic to the list of blocked content.

### Privacy notice  
 [!INCLUDE[cc_privacy_mse_bing_social_check](../includes/cc-privacy-market-insights-bing-social-check.md)]  
  
### See also  
 [Set up searches to listen to social media conversations](set-up-searches.md)   
 [Manage the quality of your search results](search-results-quality.md)   
 [Refine your search rules](refine-search-rules.md)
 
