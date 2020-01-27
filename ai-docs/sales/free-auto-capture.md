---
title: "Basic auto capture for Dynamics 365 Sales Insights | MicrosoftDocs"
keywords: 
ms.date: 01/31/2020
ms.service: crm-online
ms.custom: 
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
---

# Basic auto capture

The captured activities shown on timeline wall, rely on a set of rules, specific to the record type. For example, if you are looking at an opportunity in Sales, then timeline shows, in addition to all the activities you have logged, suggestions for up to 50 recent emails and meetings from your Microsoft Exchange account that were sent to or from the primary contact for the opportunity or its stakeholders.

You can identify the tracked and auto captured (not tracked) emails on Timeline:

1.	**Tracked emails**: This email is already being tracked, so it is already imported into Sales and is being shared with your team. A envelope symbol is used to indicate that the mail is tracked, imported into Sales, and shared with your team.

2.	**Auto capture emails**: These emails were detected by auto capture as being relevant to the current record, but they are still private so only you can see them. Compared to tracked messages, these messages show a gray symbol and a dotted border, and include a **Track** link and a private email label.

3.	**Track link**: Select the link to track an activity captured by auto capture, making it visible to everyone with access to the timeline wall of this specific record.

The activities captured by auto capture finds are only visible to you, so other members of your sales team will not be able to see them in Sales. Select the **Track** link to turn any auto capture message into a tracked email message, save the activity into the Sales database and makes it visible to other members of your team. It may take a few minutes for an activity to go from untracked to tracked, during which time it will show a **Tracking pending** message.

As with other types of activities tiles shown on the **Timeline**, click the tile to expand or collapse the activity content.

## What activities are captured?

Auto capture queries your Microsoft Exchange account and looks for activities related to the record you are looking at. The following table summarizes how auto capture identifies a related activity.

|Entity type|Matches these field values  to the To, CC, or From address of each email and meeting|  
|-----------------|--------------------------------------------------------------------------------------|  
|Account|**Email** address of the listed **Primary Contact**<br /><br /> **Email** address of the top 50 contacts that have the account as their parent account<br /><br /> All **Email** addresses defined for the account record itself.|  
|Opportunity|**Email** address listed for the **Opportunity Contact**<br /><br /> **Email** addresses of any contact in the **Stakeholders** list<br /><br /> All **Email** addresses defined for the opportunity record itself.|  
|Case|Primary contact's **Email** address<br /><br /> All **Email** addresses defined for the case record itself.<br /><br /> If the **Customer** is a contact, then use all **Email** addresses for  the contact record.<br /><br /> If the **Customer** is an account, then use all **Email** addresses for the account record|  
|Lead|**Email** address listed in the **Contact** section<br /><br /> All **Email** addresses defined for the lead record itself.|  
|Contact|All **Email** addresses defined for the contact record.|  
|Custom entities|For *account* fields, use the email address for the **Primary Contact** of the account, plus all **Email** addresses defined for the account record itself.<br /><br /> For *contact* fields, use all **Email** addresses defined for the contact record.<br /><br /> For *customer* fields that refer to a contact,  use all **Email** addresses defined for the contact record<br /><br /> For *customer* fields that refer to an account, use the **Email** address of the listed **Primary Contact**, plus all **Email** addresses defined for the account record itself.|  


### See also 

[Enable and configure auto capture](configure-auto-capture.md)

[Premium auto capture](premium-auto-capture.md)