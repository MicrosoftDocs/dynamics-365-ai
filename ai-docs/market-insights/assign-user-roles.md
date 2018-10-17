---
title: "Permissions and user roles in Market Insights | Microsoft Docs"
description: "Learn how to work with user roles and their permissions."
keywords: user roles, permissions, security, access rights
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 76e60e6f-dd1d-42ba-b2d8-a70e3f24b9c4
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
# Assign permissions and user roles

Approve and withdraw access to [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)]. Manage user permissions by assigning and editing [user roles](user-roles.md). Reach out to users by email in [!INCLUDE [pn-market-insights-short](../includes/pn-market-insights-short.md)].  
  
> [!NOTE]
>  You must be a [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] Administrator to perform these tasks.  
  
## Approve or withdraw requests  
When a self-service user signs up for a trial using an email domain that already has access to [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)], they get added to the existing tenant but can't access the service immediately. An admin needs to approve or deny their request.

## Approve a new user
  
1.  Navigate to **Settings** > **User Management**.  
  
2.  In the **Users** pane, select **Pending** from the **Status** drop-down menu.  
  
3.  Select the check boxes for the users you want to approve and select the **Edit Selected** ![edit button](media/edit-icon.png "Edit button") button.  
  
4.  In the **Edit User Role** pane, select the [user roles](user-roles.md) from the drop-down menus.  
  
5.  To confirm, select **Save** ![save button](media/save-icon.png "Save button").  

## Withdraw a request of a new user

1.  Navigate to **Settings** > **User Management**.  
  
2.  In the **Users** pane, select **Active(All)** from the **Status** drop-down menu.  
  
3.  Select the check boxes for the users you want to block from [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] and select the **Edit Selected** ![edit button](media/edit-icon.png "Edit button") button.  
  
4.  In the **Edit User Role** pane, set the **Access allowed** toggle to **No**.  
  
5.  To confirm, select **Save** ![save button](media/save-icon.png "Save button").  

  
## Change a role for a user  
  
1.  Navigate to **Settings** > **User Management**.  
  
2.  In the **Users** pane, select the list entry you want to edit.
    > [!TIP]
    >  Find licensed users using the **Search for users** input field and filter for users with a specific role by choosing a role in the **Configuration role** or **Interaction role** drop-down list.   
  
3.  In the **Edit User Role** dialog box, select the user role from the drop-down menus.  
  
4.  Click **Save** ![save button](media/save-icon.png "Save button"). The user will receive an email with the updated user roles and permissions.    
  
> [!NOTE]
> Users that are listed as [delegated administrator](delegated-admin.md) for [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] always have Administrator and Manager user roles. A lock icon ![lock button](media/lock-icon.png "Lock button") next to the user’s name indicates that you can’t change the permissions.  
  
## Send email to users
  
Use your email client to send email to [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] users. You don’t need to research a user’s email address. The email opens with the recipient’s address already filled in.  
  
1.  Navigate to **Settings** > **User Management**.  
  
2.  Identify the user you want to contact and click the **Email** ![send message button in market insights](media/enevelope-icon.png "Send message button in Market Insights") button in the **Users** list.  
  
## Privacy notice  
[!INCLUDE[cc_privacy_msl_cookies](../includes/cc-privacy-market-insights-cookies.md)]  
  
### See Also  
[Administer Market Insights](settings-administration.md)   
[Understand user roles](user-roles.md)   
[Integrate Market Insights with Office 365](manage-licenses.md)
 
