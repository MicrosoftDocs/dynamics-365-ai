---
title: "Edit an active sequence in sales accelerator | MicrosoftDocs"
description: "Learn how to edit an active sequence in sales accelerator."
ms.date: 04/09/2021
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Edit an active sequence     
When there is a change in the process of an active sequence, you can create a version of the sequence without deactivating the sequence. You can create multiple versions of a sequence, and when you assign a record to the sequence, the record is assigned to the latest version.    

>[!IMPORTANT]
>The records that were assigned to a previous version of the sequence remain connected to that version (previous).    

## Edit active sequence
1.	Sign in to your Dynamics 365 Sales Hub app.   
2.	Go to **Change area** in the lower-left corner of the page, and select **Sales Insights settings**.   
3.	Under **Sales accelerator**, select **Sequence**.   
4.	On the **Sequences** page, go to the **Active** tab, and open the sequence for which you want to create a new version.   

    > [!div class="mx-imgBorder"]
    > ![Select an active sequence to edit](media/sequence-edit-active-select-sequence.png "Select an active sequence to edit")    
 
5.	On the sequence view page, select **Edit sequence**.

    > [!div class="mx-imgBorder"]
    > ![Select edit sequence option](media/sequence-edit-active-select-edit-sequence.png "Select edit sequence option")    
 
    A confirmation message is displayed. Select **OK**.

    > [!div class="mx-imgBorder"]
    > ![Confirmation message to edit sequence](media/sequence-edit-active-sequence-confirmation.png "Confirmation message to edit sequence")    
 
6.	Edit the sequence as required and select **Save**.

    > [!div class="mx-imgBorder"]
    > ![Save the edited sequence](media/sequence-edit-active-sequence-save.png "Save the edited sequence")     

7.	On the confirmation message, provide a description of the change and select **Save**.

    > [!div class="mx-imgBorder"]
    > ![Confirmation message to save the sequence](media/sequence-edit-active-sequence-save-confirmation-message.png "Confirmation message to save the sequence")     
 
A version for the existing sequence is created and saved.

## View version history and associated records   
Viewing the version history helps you to understand the number of versions that have been created for a sequence and view the assigned records that are assigned to each version.    
1.	Open a sequence that you want to view the version history.
2.	On the sequence view page, select the **Connected *records*** tab. In this example, we are selecting **Connected leads** tab.    
    A list of leads that are connected to the sequence is displayed with the version to which they are assigned.   

    > [!div class="mx-imgBorder"]
    > ![View list of leads with associated version](media/sequence-version-view-leads-list.png "View list of leads with associated version")     
 
3.	To view the version history, select **Version history**.   
    A list of versions that are available for the sequence is displayed on the right pane.

    > [!div class="mx-imgBorder"]
    > ![Select version history option](media/sequence-version-select-version-history.png "Select version history option")     

    >[!NOTE]
    >If there are no leads attached to sequence, and you created a new version, only the latest version is displayed in the list.

### See also

[Edit a sequence](edit-a-sequence.md)  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
