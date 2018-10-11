---
title: "Domain admin takeover in Market Insights | Microsoft Docs"
description: "Perform admin takeover for an unmanged directory of an email domain."
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

# Takeover an unmanaged Market Insights directory

When a self-service user signs up for the Market Insights Preview, they are added to an unmanaged Azure Active Directory (a "shadow tenant") based on their email domain. It is a container for the accounts within Office 365 that you can’t really manage or have any controls from an organization level. If a domain admin decides to take over the unmanaged tenant as part of their managed directory, they can perform an admin takeover. The admin takeover allows an organization to administrate the organization, and be able to have more control over the users and licenses.

For detailed information, see [Take over an unmanaged directory as administrator in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover).

User data and acquired posts are merged depending on the existence of a Market Insights subscription as outlined in the sections below. 

## Admin takeover without Market Insights subscription

Perform an ["internal" admin takeover](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover#internal-admin-takeover) to get added as the global admin of the unmanaged directory and eventually integrate it a different managed tenant. Data gathered in Market Insights will still be available after admin takeover. However, users don't get migrated.
[https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover#external-admin-takeover](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-admin-takeover#external-admin-takeover)

## Admin takeover with existing Market Insights subscription

Perform an "external" admin takeover by adding the DNS domain name of the unmanaged directory to your managed Azure directory. Data from the unmanaged instance of Market Insights won't migrate to avoid overriding existing data. Users get migrated to the managed directory and so they can continue to use the service. 

### See also

[Manage connections in Market Insights](manage-connections.md)    
[Manage global settings](manage-global-settings.md)    
[Get started with Market Insights](get-started.md)