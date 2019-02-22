---
title: "Work with posts in Market Insights | Microsoft Docs"
description: "Learn how to interact with posts and how to perform internal actions."
keywords: "publish, sentiment, tag, assign"
ms.date: 01/30/2019
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 0ccac353-bd7a-438f-bf3b-de90e7a7d8b1
author: m-hartmann
ms.author: mhart
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Work with posts

(This topic is pre-release documentation and is subject to change.)

In [!INCLUDE[Dynamics 365 Market Insights](../includes/pn-market-insights-long.md)], your analysis is usually based on the posts in your data set. It’s important to understand what customers and prospects are talking about, so it’s critical to know about the actions you can take.  
  
## Change a post’s sentiment value 

In some cases the sentiment algorithm annotates a post’s sentiment differently from your perception of the tone. Adjust the sentiment value of posts if you disagree with a system-rated sentiment value. Confirm the system-rated sentiment value if you agree with it. Sentiment calculations can improve based on the users’ edits to sentiment values if the administrator [enabled adaptive learning](adaptive-learning.md).
  
1.  Select **Posts** on the right side of any Analytics page to see the posts list.  
  
     --OR--  
  
     Go to the post in your stream.  
  
2.  Select the post you want to edit and expand the contents.  
  
3.  Select the smiley face to see the sentiment value selection.  
  
4.  Edit or confirm the sentiment value of the post.  
  
> [!TIP]
>  You can confirm or edit the sentiment value of several posts at the same time when viewing them from a stream or in the post list in Analytics. To confirm or edit the sentiment value, select the check box on the left side of each post that you want to edit, and then  **Edit Sentiment**.  
  
## Add a label to a post

Outline workflows and track the status of a post by attaching a label to it. You can also filter your data by labels to find or exclude posts with specific labels. Administrators [define the labels](manage-global-settings.md#manage-labels-for-posts) to choose from in **Settings** > **Global Settings** > **Labels**.
  
> [!NOTE]
>  You must have at least a Responder interaction role to perform this task.  
  
1.  Select **Posts** on the right side of any Analytics page to see the posts list.  
  
     --OR--  
  
     Go to the post in your stream.  
  
2.  Select the posts for which you want to add or change a label.  
  
3.  Select **Set Label**, and then select the label from the list.  
  
> [!TIP]
>  You can change the label of a post at any time by overriding the existing label.  
>   
>  To remove a label from a post, select **Set Label** and then select **Clear Label**.  
  
## Assign a post to other users

Bring a post to a specific user’s attention and surface it in the user’s Inbox stream. Every user of your [!INCLUDE[Dynamics 365 Market Insights](../includes/pn-market-insights-long.md)] solution can have posts assigned. Additionally, you can assign posts to a group. You must have at least a Responder interaction role to perform this task.  
  
1.  Select **Posts** on the right side of any Analytics page to see the posts list.  
  
     --OR--  
  
     Go to the post in your stream.  
  
2.  Select the post you want to assign or reassign.  
  
3.  Select **Assign this post** ![user symbol](media/user-avatar-icon.png "User symbol").  
  
4.  In the **set assignee** menu, select **User** or **Group** in the **All user type** drop-down list.  
  
5.  Start typing and select the user or a group from the list.  
  
> [!TIP]
>  To see the posts assigned to a user or a group, apply an **Assignee** filter. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Get to know your filters](understand-filters.md)  
> 
>  For more information about groups, see [Work with Office 365 Groups in Market Insights](office-365-groups.md).  
  
## Add or remove tags 
 
[!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] lets you [add intention tags and custom tags](tags.md) to posts. Intention tags are predefined tags that are automatically added once a post is acquired. Custom tags are different from intention tags because they are not predefined and need to be manually added. Custom tags can't be automatically added to posts unless they are [promoted to auto tags](tags.md#promote-custom-tags-to-auto-tags). 
  
1.  Select **Posts** on the right side of any Analytics page to see the posts list.  
  
     --OR--  
  
2.  Go to **Social Center** to see your streams.  
  
3.  Select a post to see post details, and next to the custom tags symbol ![tag symbol in market insights](media/tag-symbol.png "Tag symbol in Market Insights"), select **Add** ![add button](media/add-icon.png "Add button"). Start typing to enter the  tag that you want to add, and then select **Confirm**.  
  
4.  To remove tags,  select **remove** ![delete button](media/delete-icon.png "Delete button") next to the tag you want to remove.  
  
## Delete posts
  
You may find posts in your data set that match one of your search topics but are irrelevant in your context. It’s easy to remove those posts. Reduce unwanted noise by deleting posts. Once a post is deleted, it can’t be restored and it will no longer count against your solution’s monthly post quota.  
  
> [!NOTE]
> - You must have at least a Power Analyst Analytics role to perform this task.  
> - You can’t undo this action, and Support can’t restore deleted posts.  
> - Deleting a post also deletes associated data like notes, sentiment edits, user assignments, labels, or information about linked [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] records assigned to a post.  
> - Please be aware that tweets which are deleted on [!INCLUDE[tn_twitter](../includes/tn-twitter.md)] will also be deleted in [!INCLUDE[Dynamics 365 Market Insights](../includes/pn-market-insights-long.md)] to meet the expectation and intent of users. 
  
### Delete posts in Analytics  
  
1.  Select **Posts** on the right side of any Analytics page to see the posts list.  
  
2.  Select the post you want to delete.  
  
3.  Select **Remove**, and then confirm your selection.  
  
### Delete posts in streams  
  
1.  Go to **Social Center**.  
  
2.  Choose your stream and a post in it.  
  
3.  Select the post to expand the contents.  
  
4.  Select **Remove** and then confirm your selection.  
  
## Link a post from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to Dynamics 365  

[!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] lets users [create a link from a post](link-posts-to-dynamics-365.md) in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to an entity in a [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] instance. When you link a post, it creates a social activity. Your administrator can [define rules to process this social activity](create-dynamics-365-record-from-social-post.md) in your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] instance. 
  
### Privacy notice 
 
[!INCLUDE[cc_privacy_msl_social_services_content](../includes/cc-privacy-market-insights-social-services-content.md)]  
  
### See Also  
 
[Drive business objectives using posts](publish-react-posts.md)   
[Analyze social data using widgets](analyze-social-data-using-widgets.md)   
[Keep track of live data streams with Social Center](social-center.md)
