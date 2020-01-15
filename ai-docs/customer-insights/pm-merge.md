---
title: "Merge process to unify data in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Learn about the merge phase in the data unification process of Dynamics 365 Customer Insights."
ms.date: 01/10/2020
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
---

# Merge

The merge phase is the last phase in the data unification process. Its purpose is reconciling conflicting data. Examples of conflicting data might be a customer name that resides in two of your datasets but shows up a little differently in each (“Grant Marshall” versus “Grant Marshal”), or a phone number format that differs slightly (617-8030-91X versus 617803091X). Merging those conflicting data points is done on an attribute-by-attribute basis.

After completing the [match phase](pm-match.md), you can start the merge phase by selecting the **Merge** tile on the **Unify** page.

## Review system recommendations

On the **Merge** page, you can choose and exclude attributes that should be merged within your unified customer profile entity (the end result of the configuration process). Note that some attributes were already auto-merged by the system.

### View merged attributes

To view the attributes that are included in one of your auto-merged attributes, select that merged attribute. The two attributes that compose that merged attribute will show up in two new rows beneath the merged attribute.

> [!div class="mx-imgBorder"]
> ![Select merged attribute](media/configure-data-merge-profile-attributes.png "Select merged attribute")

### Separate merged attributes

To separate or unmerge any of the auto-merged attributes, find the attribute in the **Profile attributes** table.

1. Select the ellipses icon.
  
2. In the drop-down menu, select **Separate fields**.

### Remove merged attributes

To exclude an attribute from the final customer profile entity, find it in the **Profile attributes** table.

1. Select the ellipses icon.
  
2. In the drop-down menu, select **Don't merge**.

   The attribute is moved to the **Removed from customer record** section.

## Manually add a merged attribute

<!--needs more details and screenshots-->

To add a merged attribute, go to the **Merge** page.

1. Select **Add merged attribute**.

2. Provide a **Name** to identify it on the **Merge** page later.

3. Optionally, provide a **Display name** that will appear in the unified Customer Profile entity.

4. Configure **Select duplicate attributes** to select the attributes that you want to merge from the matched entities. You can also search for attributes.

5. Set the **Rank by importance** to prioritize one attribute above the others. For example, if the *WebAccountCSV* entity includes the most accurate data about the *Full Names* attribute, we will prioritize this entity over *ContactCSV* by selecting *WebAccountCSV*. As a result, *WebAccountCSV* moves to first priority, while *ContactCSV* moves to second priority when pulling values for the *Full Name* attribute.

## Run your merge

Whether you manually merge attributes or let the system merge them, you can always run your merge. Select **Run** on the **Merge** page to start the process.

If you want to make additional changes and re-run the step, you can cancel a merge process while it's in progress. Select **Stop** on the notification bar while the merging of records is in progress to stop the current run.

> [!div class="mx-imgBorder"]
> ![Data merge Save and Run](media/configure-data-merge-save-run.png "Data merge Save and Run")

After the **Merge is running** message disappears, merge has completed and resolved contradictions in your data according to the policies that you have defined. Both your merged and unmerged attributes will be included in your unified profile entity, while your excluded attributes will not.

## Next Step

Configure [Activities](pm-activities.md), [Enrichment](pm-enrichment.md), or [Relationships](pm-relationships.md) to more insights about your customers.
