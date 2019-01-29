---
title: "Merge| MicrosoftDocs"
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
# Merge

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-profile-attributes.png "Merge profile attributes")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-dont-merge.png "Merge profile attributes don't merge")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")


This is the last phase within the data configuration process and it's all about reconciling conflicting data. Examples for such a conflicting data might be the customer name which resides in two of your datasets but shows a little bit different (Grant Marshall versus Grant for instance), or a phone number format that slightly differs (617-8030-91X versus 617803091X for instance). Merging those conflicting data points is done on an attribute-by-attribute basis as we will see in this section.

Once completing Match, you can access Merge via the **Merge** tile within the **Configure Data** page.

// replace

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-attribute.png "Merge add attribute")

When you ready to start the Merge process, simply click **Merge** in the following screen:

// add merge new 1

## Step One: Reviewing System Recommendations

The next screen that you will see is the **Merge screen:**

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-attribute-name.png "Merge attribute name")

The goal behind this screen is to enable you, the user, to choose all the attributes that should be merged and included in your **unified customer profile entitiy** (the end result of the configuration process). Notice that some attributes were already auto-selected by the system (highlighted in the image above). 
- The attribute's name appears in the first column (shown in red)
- The attribute's entity is specified in the second column (shown in blue)
- The attribute's data source is specified in the third column (shown in green)
- You should review those attributes and decide whether you wish to include them in your unified entity. If this is not the case for one or more of the attributes, you can click the button that is highlighted below, which will move the attribute to the **excluded from profile** section:

// add merge new 3

## Step Two: Manually adding a merged attribute
Adding a merged attribute is available via the **Add Merged Attribute** button as shown below:

// update with Merge new 4
> [!div class="mx-imgBorder"] 
> ![](media/merge-add-merge-attribute.png "Add merged attributes")

We will perform the manual merge process within the **Add Merged Attribute** panel as shown below. This panel consists of three parts: **Name** (shown in red), **Unmerged Entities** (shown in blue) and **Merge Policy** (highlighted in green): 

// update with Merge new 5
> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-add-new-name.png "Add new attributes")

First we will type an attribute name in the **Name** field. For exemplification, we will define the merged attribute **Name**.
 
Then we will search for attributes that might correspond to that attribute within our matched entities by typing **Name** in the **Unmerged Entities** field as shown below:

// update with merge new 6
> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-image10.png "Image 10")

Third, within the menu highlighted in red above, we will select all the attributes that we want to merge from our matched entities. As shown, we have selected **First Name** from **Sales**, **Name** from **SurveyContact** and **Name** from **WifiContact**.

**Lastly, we will define the Merge Policy:** Here we will prioritize one source above the others - the values for our merged attribute will come only from that source. If we think, for example, that the **Sales** entity includes the most accurate data about the **Names** attribute, than in the panel shown below, we will first change the policy from **default** to **ordered** (as highlighted in blue) and then click the arrow sign next to **SurveyContact**. As a result **Sales** will move to first priority while **SurveyContact** will move to second priority when pulling values for the **Name** attribute.

// update with merge new 7
> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-image11.png "Image 11")

## Step Three: Running your merge
Whether you manually merge attributes or let the system merge for you, at this point you can run your merge. Simply click **Save** and then **Run** at top of the screen. Note that **if the *Run* button is disabled at this point, you should try to do two things.

**First,** try to refresh your page and see if this button turns active:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-image18.png "Image 18")

**Second**, try to go back to the **Match** screen and hit the **Run** button in this screen again. Go back to the **Merge** screen and see if that resolved the problem.

Once the message below disappears, Merge has completed and resolved contradictions in your data according to the policies that you have defined. **All your merged attributes will be included in your unified profile entity and vice versa**.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-image17.png "Image 17")

## Step Four: Validating your merge
Couple of options are available for you to validate the quality of your merge processess. -> complete!
  
## Next Step
**Congratulations!** You have completed both the **Data Manager** and the **Configure Data** phases. Now you are ready to unlock unique insights on your customers via the **Segmentation**, **Connectors** sections as well as the **APIs** section if you are a technical user. Note that **Segmentation** will equip you with aggregate-level insights, while **Connectors** will enable you to unlock insights on specific customers.
 
