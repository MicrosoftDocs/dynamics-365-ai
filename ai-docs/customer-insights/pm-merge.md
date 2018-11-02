---
title: "Merge| MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/31/2018
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

Once completing Match, you can access Merge via the **Merge tile** within the **Configure Data** screen:

[final 1]

This is the last phase within the data configuration process and it's all about reconciling conflicting data. Examples for such a conflicting data might be the customer name which resides in two of your datasets but shows a little bit different (Grant Marshall versus Grant for instance), or a phone number format that slightly differs (617-8030-91X versus 617803091X for instance). Merging those conflicting data points is done on an attribute-by-attribute basis as we will see in this section.

## Step One: Deciding Between a System Merge and a Manual Merge

The first screen that you will see is the following screen:

[final 2]

- The tiles at the top of the screen (highlighted in green above) show that you haven't tried to merge any attributes yet. **All Attributes** shows how many attributes your matched entities include **in total prior to Merge**. You can revisit your Match policies if you suspect that this number is too low or high. **Discarded Attributes** are attributes that were not included in the merge process and at this point their number equals the **All Attributes** number since no merge process has started yet.

- The goal behind this screen is to equip you, the user, with two approaches to the merge process: 
  -**Option One: Letting the system auto-identify attributes anmong your entities that should be merged**. For choosing that option, click **System Merge** as highlighted in blue above. Note that you can always manually select more attributes to Merge.
  -**Option Two: Manually defining all the attributes that, among your matched entities, should be merged**.
  
**Important note:** If you chose option one, then you should continue through steps 2 and 3 below and possibly also throguh step 4 if you wish to merge more attributes. If you chose option two however, first go through step 4 in this section and then come back to steps 2 and 3.

## Step Two: Understanding the Merge screen

[final 3]

The **Merge screen** that is shown above includes several components, regardless of your choice in step one. We will explore them below:
- **Four validation tiles** (shown below): By tracking those tiles as you work with the Merge screen you can keep validating the quality of your merge selections. Beyond the **All Attributes** and **Discarded Attributes** tiles that we discussed earlier, there are two more important tiles:
    - **Merged Attributes** tile shows how many attributes were successfully merged from multiple (matched) entities. It should answer the expectations that you have around your specific data. 
    - **Unmerged Attributes** tile shoes how many attributes were not successfully merged by the system.
    
    [final 4]

- **Left Attributes Menu**: This menu includes three expendable tabs:
    - **Merged Attributes**: Upon clicking it you can view the attributes that were merged at this point as exemplified below in red:
     
     [final 5]
     
     Note that within the blue part above, you can also see what entity was used as the main source for that merged attribute. In the example above, the values of the merged attribute **IdentityServiceEmail** were taken in most cases from the **SurveyContact** entity (reflected by a value of 1 in the **order** column) and in less cases from the **Sales** entity (reflected by an **order** value of 2).
     
    - **Unmerged Attributes**: Upon clicking it you can view what attributes were not merged by the system( shoen in red below). Again, you can also see from which entity the values of this entity come from (but since it's unmerged attribute it's values come from only one entity):
    
    [final 6]
    
    - **Discarded Attributes**: Same options exist for this tab as for the **Unmerged Attributes** tab.
    
    [final 7]
    
At this point, if you suspect that some important attributes were not matched, you can manually add them through the **Add Merged Attribute** button. We will expand on adding merged attributes in the next step. If, on the contrary, you suspect that too many attributes are merged at this point, you can unmerge them by clicking the **three dots** icon as shown below and then **Unmerge**:
    
   [final 8]
    
- **Right attribute values table**: Upon clicking each of the attributes in the **left attributes menu** a corresponding attribute values table will appear to the right:

[final 9]

This table's fields represent the different entities in which this selected attribute exists. Within the example above...

## Step Three: Changing Merging Policies for Merged Attributes

![merge-single-attribute.png](media/merge-single-attribute.png)

- **Prioritizing sources for pre-identified merged attributes**: Using the attribute *Name* as an example, in this section we will learn how to prioritize contradicting values for that attribute as part of the merging process. We start by selecting <b>...</b> below: 

![merge-single-attribute-edit.png](media/merge-single-attribute-edit.png)

- We will conduct the prioritization process within the **Edit Attribute Panel** as shown below. This panel consists of three parts: **Attribute Name** (shown in red below), **Attribute Source** (shown in blue) and **Merge Policy** (shoen in green): 

![merge-experiment-datasource-dropdown.png](media/merge-experiment-datasource-dropdown.png)

  - First we will consider to edit the **Attribute Source** part. This part specifies all the matched entities that include values for the *Name* attribute. we can see that by default, all these sources are selected and hence values for the *Name* attribute are taken into consideration from all three sources. If we wish **not** to consider one or more of the sources we will **unselect** them.
  
  - Second, we will consider to edit the **Merge Policy** part. This part specifies only the sources that were selected within **Attribute Source**. Here we will prioritize those sources: If we think for example that *Dynamics WiFidata* includes the most accurate data about *Names*, than in the panel shown above, we will first change the policy from **default** to **ordered** and then click the arrow sign next to *Salesforce Sales Data*. As a result *Salesforce Sales Data* will move to first priority while *Dynamics WiFidata* will move to second priority when pulling values for the *Name* attribute.
  
  - Lastly, hit **Save** at the top right corner of this panel.

## Step 4: Manually adding a merged attribute**: 
Adding a merged attribute is available via the **Add Attribute** option as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/merge-add-merge-attribute.png "Add merged attributes")

- We will perform the attribute addition process within the **Add Attribute** panel as shown below. This panel consists of three parts: **Attribute Name** (shown in red), **Select Attributes** (shown in blue) and **Merge Policy** (shown in green). 

![merge-experiment-datasource-dropdown.png](media/merge-experiment-datasource-dropdown.png)

  - First we will type an attribute name in the **Attribute Name** field. This name should be informative - a name that help us understand how this attribute was constructed  
  - Then, within the **Select Attributes** menu, we will select all the attributes that we want to merge from our matched entities
  - Lastly, we will define the merge policy by clicking on the relevant arrows in the *Merge Policy* section as we did before.
  
- **Editing a group merged attribute**: In some cases, it will be valuable to group multiple attributes as one merged attribute. In the example shown below, the attribute *Address* is defined as a group attribute as represented by the icon next to it (such icon doesn't appear next to single attributes). The table shown includes all the attributes that are included in the group attribute.
  
![merge-group-attributes-dropdown.png](media/merge-group-attributes-dropdown.png)

   - In order to edit a group attribute, we will click on the *three dots* icon just as we used to do for a single attribute.
   - In the next stage, we will use the *Edit Group Attribute* panel that is shown below. We want to find all the attributes that should be included in this group attribute and we will achieve that by typing those attributes names in the *search* field.
     
 ![merge-group-attributes-edit.png](media/merge-group-attributes-edit.png)
 
