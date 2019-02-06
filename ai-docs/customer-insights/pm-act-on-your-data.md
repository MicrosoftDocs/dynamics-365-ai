---
title: "Act on your data | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
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
robots: noindex,nofollow
---
# Act on your data

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

- **Exporting a Segment:** That can be done both to a csv. file and to a Dynamics 365 location.

    1. Both options are available within the *Segments page*: 
      - First click the **three dots icon** within a specific segment's tile: 
      // missing 1
      - Then select the **Export** button: 
      // missing 2
      - Lastly, choose between a csv. format and a specific Dynamics 365 destination. To add a destination, use the **Export Screen** as explained below (this screen is accessable via the **Export Segment** tab on the left side menu).
      
    2. Both options are also available within the specific segment's page by clicking **Export** at the top-right corner of the page:

    > [!div class="mx-imgBorder"] 
    > ![](media/segment-menu-export-top.png "Export segment")
    

- **Adding an Export Segment Destination**:
    1. **Within the Segment Export screen**, click **Add Destination:**

    > [!div class="mx-imgBorder"] 
    > ![](media/segmentation-add-destination.png "Segmentation add destination")

    2. Give your destination a recognizable name, define it's URL, and select a Dynamics 365 account:

    > [!div class="mx-imgBorder"] 
    > ![](media/segmentation-export-destination.png "Segmentation export destination")

    3. Upon the completion of step 3, your destination should appear in the **Destinations** table as shown in the example below:

    > [!div class="mx-imgBorder"] 
    > ![](media/segmentation-export-destination-actions.png "Segmentation export destination table")

 - **Viewing Segments you have Exported**:
    That can be done also in the Export Segmnet screen. Below the Destinations table you can find another table, called **Exported Segments** which specifies important information around the segments you have exported: 
    
    // missing 3
