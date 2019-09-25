---
title: "Get suggestive action on notes for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Get intelligent suggestions on action that you take on notes you enter during a recent meeting or discussion with your customer."
ms.date: 10/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
ms.assetid: aabede7c-a3fa-459d-a237-1f1d03ba3e62
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# How Notes analysis assists you with suggestion

[!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] allows you to view and quickly enter notes on **Timeline** control (formerly known as activity wall). When you enter notes regarding a recent meeting or discussion with your customer, [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] monitors these notes and gives you intelligent suggestions. With these suggestions, you can save time and effort by taking actions such as creating a meeting request and adding a contact then and there on the note.<br>
**Timeline** control is available on contacts, opportunities, leads, accounts, and case forms.<br> 
 > [!div class="mx-imgBorder"]
 > ![Suggested actions on Timeline control](media/notesanalysis-timelinecontrol.png "Suggested actions on Timeline control")<br>
When you save a note, the text in the note is highlighted and when selected, suggestions are displayed. These suggestions include: Creating activities, tasks, contacts, meeting, content requests, and issue detection.<br>
For example, you created a note “*Meet the customer on the May 4 at 4:00 PM*”. When you select this text, [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] provides an automatic suggestion to create an appointment.<br>
 > [!div class="mx-imgBorder"]
 > ![Create an appointment](media/notesanalysis_createappointment.png "Create an appointment")<br>
When you have multiple suggestions associated with a note, [!INCLUDE[pn-dyn-365-sales](../includes/pn-dyn-365-sales.md)] displays those multiple suggestions—you can take timely actions depending on your requirements. For example, you have created a note to contact your customer regarding pricing and schedule a meeting to further discuss the deal. The note shows suggestions to create an appointment and schedule a phone call. Let's look this example to see how suggestion-based notes work with multiple suggestions:<br>
1.	Open a record with the note and select the note text. <br> 
    In this example, the note specifies to call Debra to discuss the pricing of deal and schedule a meeting to discuss meeting.<br>
    > [!div class="mx-imgBorder"]
    > ![Schedule a meeting](media/notesanalysis-schedulemeeting.png "Schedule a meeting")<br>
    Suggestions to create an appointment and a phone call are displayed.<br>
    > [!div class="mx-imgBorder"]
    > ![Multiple suggestions](media/notesanalysis-multiplesuggestions.png "Multiple suggestions")<br>
    Use the arrow icon to switch between the suggestions.
2.	On the **New Appointment suggestion** card, select **Edit and Create**.<br>
    The **Quick Create: Appointment** form opens with prefilled information from the note.<br>
    > [!div class="mx-imgBorder"]
    > ![Quick create appointment](media/notesanalysis-quickcreateappointment.png "Quick create appointment")<br>
3.	Edit the necessary information and select **Save**.
4.	Similarly, repeat step 2 and 3 for New phone call suggestion.<br>
    A new appointment and a call are scheduled for the record.<br>

[!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Work with activities](/dynamics365/customer-engagement/basics/work-with-activities)


## Examples

The following three scenarios are the examples of how to use notes analysis in your organization.

- [Scenario 1: Suggest New Contact](#scenario-1-suggest-new-contact)
- [Scenario 2: Suggest Task Creation](#scenario-2-suggest-task-creation)
- [Scenario 3: New Meeting](#scenario-3-new-meeting)


### Scenario 1: Suggest New Contact

   - Let me introduce you to John
    
### Scenario 2: Suggest Task Creation

   - I will prepare the contract by Friday.
   - John to confirm the date with Contoso.
   - John, can you please send the code to them?
 
### Scenario 3: New Meeting

   - Could we talk over coffee while I am in town?
   - We had a meeting with Contoso last Friday.

## Privacy notice  

For specific privacy information about [!INCLUDE[pn_dynamics_sales_insights](../includes/pn-dynamics-sales-insights.md)] capabilities for sellers, see [Privacy notice](privacy-notice-seller.md).

### See also

[Configure Dynamics 365 Sales Insights](configure-enable-dynamics-365-ai-sales.md)