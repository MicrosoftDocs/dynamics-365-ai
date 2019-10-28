---
title: "Learn how to work with meetings in Dynamics 365 assistant app | MicrosoftDocs"
description: "Learn how to work with meetings in Dynamics 365 assistant app."
keywords: " "
ms.date: 10/01/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: 8f433c64-e57b-43a6-b57c-3bf75d2255f6
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Working with meetings

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]
> - Microsoft doesn't provide support for this preview feature. Microsoft Dynamics 365 Technical Support won’t be able to help you with issues or questions. Preview features aren't meant for production use and are subject to a separate [supplemental terms of use](https://go.microsoft.com/fwlink/p/?linkid=870960).

The Dynamics 365 assistant app for Microsoft Teams provides information about your daily meetings on your mobile device. This helps you to prepare for an upcoming meeting so that you can build a strong relationship with customers. These meetings display the list of participants who are external and not in your organization. The app displays meetings related to your current day and keeps you up to date by syncing in real time with your Office 365 account. 

The meetings provide basic information such as subject, time and location, participants, regarding entities, and related entities. 

> [!div class="mx-imgBorder"]
> ![Meeting preparation page](media/si-teams-app-meeting-preparations.png "Meeting preparation page") 

To view more details, select and open the meeting. The **Meeting preparation** page opens with detailed information. 

> [!div class="mx-imgBorder"]
> ![Meeting page with more details](media/si-teams-app-meeting-preparations-more-details.png "Meeting page with more details")  

The meeting preparation page is typically divided into the following sections:

1.	[Meeting information](#meeting-information) 

2.	[Participants](#participants)

3.	[Regarding entity](#regarding-entity)

4.	[Activity timeline and insight cards](#activities-timeline-and-insight-cards)

## Meeting information

The meeting preparation section provides information on the subject, when the meeting is scheduled, and where the meeting is happening. This information is view-only. You cannot edit it in the app. 

## Participants

Participants are the customers and the organizer who are attending the meeting. You can see who will attend with the acceptance status such as accepted, tentative, and declined. 

### Add new customer contact

If any customers in the participant list are not in your contacts, you can add them to the contact list in the Dynamics 365 Sales organization. These contacts are displayed under the **NEW CONTACT** section. 


Select the contact and the contact opens. At the bottom of the customer details page, select **Add to Dynamics 365**. The customer is added to the contact list in the Dynamics 365 Sales organization.

### View details of a customer

To view more details about a customer, select the contact. The following details are displayed:

-	Contact information for the customer such as mobile number and business email.

-	Colleagues in your organization who know and can introduce you to this contact. To learn more, see [How to get introduced to a lead](who-knows-whom.md).

-	Talking points to start a conversation with the added customer. To learn more, see [Know conversation starters for your customers](talking-points.md).

## Regarding entity

The regarding entity specifies what the meeting is about, such as opportunity, lead, contact, or account. When a meeting is attached to an entity, the meeting displays the timeline, insight, participant information, and corresponding related entities. Also, the regarding entity helps you to understand what the meeting is about, so you can come prepared with relevant information.

In the following image, you can see that the meeting is regarding an opportunity that has 10 orders of product... .

> [!div class="mx-imgBorder"]
> ![Regarding entity](media/si-teams-app-regarding-entity.png "Regarding entity")

### View regarding and related entities

To view more details about the regarding entities, select the entity. The details such as timeline activities and relevant cards are displayed along with related entities cards. Also, related entities are displayed if any related entities are attached to the regarding entity. You can swipe to view the related entities. 

> [!div class="mx-imgBorder"]
> ![Regarding entity detailed view](media/si-teams-app-regarding-entity-details.png "Regarding entity detailed view")

To view the entity in the Dynamics 365 assistant application, from the **REGARDING** section, select more options (**…**) and then select **Open in Dynamics 365**.

### Add regarding entity

You can add a regarding entity to a meeting when no regarding entity is attached to it. When you add the regarding entity, its corresponding related entities are also added to the meeting. 

> [!NOTE]
> Once you add a regarding entity, you cannot delete it. However, you can update the entity if you find the added entity is inappropriate. 

To add a regarding entity, follow these steps:

1.	On the meeting card, select **Set regarding**.

    > [!div class="mx-imgBorder"]
    > ![Add regarding entity through set regarding option](media/si-teams-app-set-regarding-option.png "Add regarding entity through set regarding option") 

    -OR-

    On the **Meeting preparation** page, under the **REGARDING** section, select **Set regarding**. 

    > [!div class="mx-imgBorder"]
    > ![Add regarding entity through set regarding option](media/si-teams-app-set-regarding-option-section.png "Add regarding entity through set regarding option") 

2.	On the **Set regarding** page, select a regarding field from the list of entities.

    > [!div class="mx-imgBorder"]
    > ![Add regarding entity through set regarding option](media/si-teams-app-search-regarding-entity.png "Add regarding entity through set regarding option")
 
    The regarding entity is added to the meeting along with its corresponding related entities.

### Update regarding entity

You can update the regarding entity when it no longer is relevant or there are changes to the meeting. To update the regarding entity, follow these steps:

1.	Select and open the meeting. The **Meeting preparation** page opens with detailed information.

2.	From the **REGARDING** section, select more options (**…**) and then select **Change regarding record**.

## Activities timeline and insight cards

See a combined view of your interactions with customers across various channels, such as phone, email, or even social activities in the timeline that are related to the regarding entity. The timeline also shows any related notes or system posts. Also, cards are displayed below the timeline based on the related entities.

The timeline activities and cards are retrieved from your Dynamics 365 Sales organization for the selected regarding entity.

The following image is an example of an activity timeline for an opportunity regarding entity.

> [!div class="mx-imgBorder"]
> ![Activities timeline and insight cards page](media/si-teams-app-activities-timeline-insights-cards.png "Activities timeline and insight cards page")

### See also

[Install Dynamics 365 assistant application on Microsoft Teams](install-assistant-application-microsoft-teams.md)

[Overview of Dynamics 365 assistant application](overview-dynamics-365-assistant-app-teams.md)
