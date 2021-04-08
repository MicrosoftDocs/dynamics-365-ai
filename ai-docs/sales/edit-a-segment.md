---
title: "Edit a segment in the sales accelerator | MicrosoftDocs"
description: "Learn how to edit a segment in the sales accelerator."
ms.date: 04/09/2021
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Edit a segment

To modify your process for choosing the records you want as members of a segment, you can update the conditions that you've defined in the segment.<!--note from editor: Edit okay? "Members of a segment" echoes the intro to create-and-activate-a-segment.md -->

1.	Sign in to your Dynamics 365 Sales Hub app.   
2.	Go to **Change area** in the lower-left corner of the page, and select **Sales Insights settings**.
3.	Under **Sales accelerator**, select **Segments**.   

    The **Segments** page opens with the list of available segments.   

    >[!div class="mx-imgBorder"]
    >![Segments page with a list of segments](media/sa-segment-edit-list-lead-segments.png "Segments page with a list of segments")  

4.	Select and open the segment that you want to edit. In this example, **Leads from contact us** is selected.

    >[!div class="mx-imgBorder"]
    >![Select a lead to edit](media/sa-segment-edit-select-lead.png "Select a lead to edit")  
 
5.	Select **Edit**. 
6.	On the confirmation message, select **Edit**.

    >[!div class="mx-imgBorder"]
    >![Edit confirmation message](media/sa-segment-edit-lead-edit-confirmation.png "Edit confirmation message")  
  
7.	Edit the conditions, select **Save**, and then in the confirmation message that appears, select **Update segment**.

    >[!div class="mx-imgBorder"]
    >![Save your edits](media/sa-segment-edit-lead-edit-save-confirmation.png "Save your edits")  

The changes will be applied to records that are created in the future in the application<!--note from editor: I don't know what "created in the application for this segment" means - aren't records just created, and then the conditions of the segment are applied to them and they either become members of the segment, or they don't?-->. The records that are already members of this segment won't change.<!--note from editor: Edit okay? Should this say "The records that the segment has already been applied to won't change"? -->

### See also

[Create and activate a segment](create-and-activate-a-segment.md)   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
