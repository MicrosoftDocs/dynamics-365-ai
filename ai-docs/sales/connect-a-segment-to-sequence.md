---
title: "Connect a segment to sequence in the sales accelerator | MicrosoftDocs"
description: "Learn how to connect a segment to sequence in sales accelerator."
ms.date: 04/09/2021
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Connect a segment to sequence 

After you create and activate a segment, you connect the segment to sequence depending on the entity that you've created the sequence for. You can add segments to existing sequences. Open the sequences to view details and then add segments to them. Follow these steps:   

1.	Sign in to your Dynamics 365 Sales Hub app.    
2.	Go to **Change area** in the lower-left corner of the page and select **Sales Insights settings**.    
3.	Under **Sales accelerator**, select **Sequence**.    
4.	On the **Sequences** page, select the **Active** tab.    
5.	Select and open the sequence and go to **Connected Lead** tab.    
    >[!NOTE]
    > To know more on how to view details of a sequence, see [View details of a sequence and its connected records](view-sequence-details-connected-records.md).   

    >[!div class="mx-imgBorder"]
    >![View connected lead tab](media/sa-segment-connect-lead-tab.png "View connected lead tab")       

6.	From the **Connected segments** section, select **+ Connect segments**.    
    A list of available segments is displayed in the Connect records window. If there are no segments associated with the sequence, an empty grid is displayed.

    1.	Select the segments that you want to apply for the sequence.    
        In this example, the segments, Leads from contact us form, North USA leads interested in printers, and South USA leads interested in laptops are selected.    

        >[!div class="mx-imgBorder"]
        >![Select segments to connect to sequence](media/sa-segment-connect-select-segments.png "Select segments to connect to sequence")       

    2.	Select **Connect**. The selected segments are added to the sequence with details such as status, owner, and number of records associated with the segment.   

        >[!div class="mx-imgBorder"]
        >![Selected segments added to sequence](media/sa-segment-connect-selected-segments-added.png "Selected segments added to sequence")      

    3.	Open each associated segment and choose which records you want to connect to this sequence.    

        >[!NOTE]
        >To disassociate a segment with this sequence, select the segment and then select **Disconnect**. On the confirmation message, select **Disconnect** segment.   
8.	Close the sequence.

### See also

[Create and activate a segment](create-and-activate-a-segment.md)   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
