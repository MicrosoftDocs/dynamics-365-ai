---
title: "Domain admin takeover in Market Insights | Microsoft Docs"
description: "Perform admin takeover for an unmanaged directory of an email domain."
keywords: "admin takeover, tenant, self-service user"
ms.date: 10/31/2018
ms.service: dynamics-365-marketing
ms.topic: article
ms.assetid: fb81eeb9-c0b5-476f-83c9-d566c3352dd3
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.custom: 
  - dyn365-a11y
  - dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Take over an unmanaged directory that has Market Insights

(This topic is pre-release documentation and is subject to change.)

Market Insights' self-service sign-up allows any user with a work email to get the app. When users sign up with an email domain that is not registered in Azure Active Directory (Azure AD), they are added to an unmanaged Azure AD (a "shadow tenant") based on their email domain. This is a container for the accounts within Office 365 that you can’t really manage or control from an organizational level. If a domain admin decides to take over the unmanaged tenant as part of their managed directory, they can perform an admin takeover. The admin takeover allows an admin to manage the organization, and have more control over the users and licenses.

For detailed information, see [Take over an unmanaged directory as administrator in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover).

User data and acquired posts are merged depending on the existence of a Market Insights subscription as outlined in the sections below. 

## Admin takeover without Market Insights subscription

When the domain admin takes over the unmanaged directory, if their managed directory *does not already have* a Market Insights or Microsoft Social Engagement subscription, the Market Insights solution with the data will be available after admin takeover.

## Admin takeover with existing Market Insights subscription

When the domain admin takes over the unmanaged directory, if their managed directory *already has* a Market Insights or Microsoft Social Engagement subscription, data from the Market Insights solution will not be migrated. An administrator in Market Insights must explicitly [approve access for users](assign-user-roles.md#approve-a-new-user) migrated over from the unmanaged directory after the takeover. 

### See also

[Manage connections in Market Insights](manage-connections.md)    
[Manage global settings](manage-global-settings.md)    
[Get started with Market Insights](get-started.md)
