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

This is the last phase within the data configuration process and it's all about reconciling conflicting data. Examples for such a conflicting data might be the customer name which resides in two of your datasets but shows a little bit different (Grant Marshall versus Grant for instance), or a phone number format that slightly differs (617-8030-91X versus 617803091X for instance). Merging those conflicting data points is done on an attribute-by-attribute basis as we will see in this section.

Once completing Match, you can access Merge via the **Merge** tile within the **Configure Data** page.

## Step One: Reviewing System Recommendations

The next screen that you will see is the **Merge screen:**

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-profile-attributes-full-name.png "Merge profile attribute full name")

There are two goals behind this screen:
- 1.**Choosing all the attributes that should be merged within your unified customer profile entitiy** (the end result of the configuration process). Notice that some attributes were already auto-merged by the system (highlighted in the image above):
- The attribute's name appears in the first column 
- The attribute's entity is specified in the second column 
- The attribute's data source is specified in the third column 
- If you wish to view what attributes that are included in one of your auto-merged attributes, click that merged attribute. The two attributes that compose that merged attribute will show up in two new rows beneath the merged attribute:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-profile-attributes.png "Merge profile attributes")

- If you wish to unmerge any of these auto-merged attributes, use the button shown below and click **Don't Merge**:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-profile-attributes-add-merged.png "Merge profile attribute")

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-profile-attributes2.png "Merge profile attributes")

- 2.**Excluding attributes from the customer profile entity:** If you think that some attributes should be excluded from the final customer profile entiy, you can click the same button used for unmerging but this time choose **Exclude**:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-dont-merge.png "Merge profile attributes don't merge")

That will move the attribute/s to the **excluded from profile** section:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-exclude-from-profile.png "Merge excluded from profile")

## Step Two: Manually adding a merged attribute
Adding a merged attribute is available via the **Add Merged Attribute** button as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/merge-add-merge-attribute.png "Add merged attributes")

We will perform the manual merge process within the **Add Merged Attribute** panel:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-attribute-name2.png "Merge attribute name")

This panel consists of three parts:

**Name**: First we will type an attribute name (so we can identify it in the Merge screen later).

**Display Name**: Then we will determine how we want our merged attribute to be named in our final Customer Profile dataset.

**Select Duplicate Attribute**: Within this menu we will select all the attributes that we want to merge from our matched entities. We can also use the search field to type our attributs' names. 

**Rank by Importance:** Here we will prioritize one attribute above the others - the values for our merged attribute will come only from that source. If we think, for example, that the **Sales** entity includes the most accurate data about the **Names** attribute, than in the panel shown below, we will first change the policy from **default** to **ordered** (as highlighted in blue) and then click the arrow sign next to **SurveyContact**. As a result **Sales** will move to first priority while **SurveyContact** will move to second priority when pulling values for the **Name** attribute.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-attributes2.png "Merge attributes")

## Step Three: Running your merge
Whether you manually merge attributes or let the system merge for you, at this point you can run your merge. Simply click **Save** and then **Run** at top of the screen. Note that **if the *Run* button is disabled at this point, you should try to do two things.

**First,** try to refresh your page and see if this button turns active:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-image18.png "Image 18")

**Second**, try to go back to the **Match** screen and hit the **Run** button in this screen again. Go back to the **Merge** screen and see if that resolved the problem.

Once the message below disappears, Merge has completed and resolved contradictions in your data according to the policies that you have defined. **All your merged attributes will be included in your unified profile entity and vice versa**.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-merge-image17.png "Image 17")
  
## Next Step
**Congratulations!** You have completed both the **Data Manager** and the **Configure Data** phases. Now you are ready to unlock unique insights on your customers via the **Segmentation**, **Connectors** sections as well as the **APIs** section if you are a technical user. Note that **Segmentation** will equip you with aggregate-level insights, while **Connectors** will enable you to unlock insights on specific customers.
 
