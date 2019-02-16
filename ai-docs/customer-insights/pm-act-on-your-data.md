---
title: "Export Segment | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/20/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# Export Segment

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Exporting a segment

This can be done both to a CSV file and to a Customer Engagement location.

1. Both options are available within the **Segments** page.
      
   - First click the **three dots icon** within a specific segment's tile (shown in red below)
   - Then click the **export** option from the actions menu (shown in blue)
   - Lastly, choose between a csv. format and a specific Dynamics 365 for Sales destination (shown in green below). Note: At this point only Dynamics 365 for Sales destinations are supported. 
      
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-csv.png "Segmentation export")
      
       To add a destination, use the **Export Screen** as explained below (this screen is accessible via the **Export Segment** tab on the left side menu).
      
2. The csv. option is also available within the specific segment's page by clicking **Export** at the top-right corner of the page:

   > [!div class="mx-imgBorder"] 
   > ![](media/segment-menu-export-top.png "Export segment")
    

## Adding an export segment destination

1. Within the **Segment Export** page, select **Add Destination**.

   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-add-destination.png "Segmentation add destination")

2. Give your destination a recognizable name, define it's URL, and select a Dynamics 365 for Sales account.

   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-destination.png "Segmentation export destination")

3. Upon the completion of Step 3, your destination should appear in the **Destinations** table. Below you can see an example with three created destinations. Beyond the details completed in Step 2, this table also specifies the creation date and time for your destinations.

   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-destination2.png "Segmentation add destination")
    
   Your saved destination will also light up in the **Segments** page under the export option we explored earlier.
    
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-in-process.png "Segmentation export in process")
    
   Upon clicking your Dynamics 365 for Sales destination (shown in red above), you should wait until the exporting process has completed. As long as it's in progress you can expect to see the following message.
    
   > [!div class="mx-imgBorder"] 
   > ![](media/segmentation-export-destination3.png "Segmentation destination")

## Viewing segments you have exported

That can be done also in the **Export Segment** page. Below the **Destinations** table you can find another table, called **Exported Segments** which specifies important information around the segments you have exported.
    
> [!div class="mx-imgBorder"] 
> ![](media/segmentation-export-segments.png "Segmentation export segments")


## Deleting a destination

That can be done via **Delete** in the **Export Segment** page.

   // image 6
