---
title: "Prerequisites to administer Conversation Intelligence | MicrosoftDocs"
description: "Prerequisites on how to administer Conversation Intelligence"
ms.date: 06/01/2020
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 6ee1a5cf-bb4a-46d5-b835-c0ac6644dec5
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Prerequisites to configure Conversation Intelligence

Verify the following requirements before setting up Conversation Intelligence for your organization:

-	You must have an administrator or similar role.

-	You must have a Dynamics 365 Sales organization. 

-	You must purchase a [Dynamics 365 Sales Insights](https://portal.office.com/Signup/MainSignUp.aspx?OfferId=5be85c9f-df71-4bcf-ac2f-b2a05b4a1f99) license. 
    
    >[!NOTE]
    >The Sales Insights license provides you access to the Conversation Intelligence feature with 3 hours of call processing capacity for all licensed users from your organization.<br> 
    >To extend the capacity of processing hours for your organization, you must purchase the Conversation Intelligence add-on for Sales Insights.<br>
    >To learn more, see **Add-on Capacities** section in **Appendix F: Dynamics 365 Capacity Add-ons** from [Microsoft Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).
    
-	You must get access to Conversation Intelligence. If you don't have access, follow these steps:
    
    1.	To access the app, go to [Conversation Intelligence](https://sales.ai.dynamics.com/).
    
    2.	Enter your work email address.
    
    3.	When the application recognizes the email, you must sign in using Azure Active Directory. To learn more, see [Azure AD Connect user sign-in options](https://docs.microsoft.com/azure/active-directory/hybrid/plan-connect-user-signin).

-	You must create a v2 storage account with an Azure subscription to create blob container to configure call data. To learn more, see [Create a storage account](https://docs.microsoft.com/azure/storage/common/storage-quickstart-create-account?tabs=portal#create-a-storage-account-1).

### See also

[Introduction to administer Conversation Intelligence](intro-admin-guide-sales-insights.md#administer-conversation-intelligence)

[Overview of Conversation Intelligence](dynamics365-sales-insights-app.md) 
