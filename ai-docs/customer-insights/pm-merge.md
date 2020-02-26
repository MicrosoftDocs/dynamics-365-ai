---
title: "Merge process to unify data in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Learn about the merge phase in the data unification process of Dynamics 365 Customer Insights."
ms.date: 02/25/2020
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
---

# Merge

The merge phase is the last phase in the data unification process. Its purpose is reconciling conflicting data. Examples of conflicting data could include a customer name found in two of your datasets but that shows up a little differently in each (“Grant Marshall” versus “Grant Marshal”), or a phone number that differs in format (617-803-091X versus 617803091X). Merging those conflicting data points is done on an attribute-by-attribute basis.

After completing the [match phase](pm-match.md), you start the merge phase by selecting the **Merge** tile on the **Unify** page.

## Review system recommendations

On the **Merge** page, you choose and exclude attributes to merge within your unified customer profile entity (the result of the configuration process). Some attributes are automatically merged by the system.

### View merged attributes

To view the attributes that are included in one of your automatically merged attributes, select that merged attribute. The two attributes that compose that merged attribute display in two new rows beneath the merged attribute.

> [!div class="mx-imgBorder"]
> ![Select merged attribute](media/configure-data-merge-profile-attributes.png "Select merged attribute")

### Separate merged attributes

To separate or unmerge any of the automatically merged attributes, find the attribute in the **Profile attributes** table.

1. Select the ellipsis (...) button.
  
2. In the dropdown list, select **Separate fields**.

### Remove merged attributes

To exclude an attribute from the final customer profile entity, find it in the **Profile attributes** table.

1. Select the ellipsis (...) button.
  
2. In the dropdown list, select **Don't merge**.

   The attribute is moved to the **Removed from customer record** section.

## Manually add a merged attribute

To add a merged attribute, go to the **Merge** page.

1. Select **Add merged attribute**.

2. Provide a **Name** to identify it on the **Merge** page later.

3. Optionally, provide a **Display name** to appear in the unified Customer Profile entity.

4. Configure **Select duplicate attributes** to select the attributes that you want to merge from the matched entities. You can also search for attributes.

5. Set the **Rank by importance** to prioritize one attribute above the others. For example, if the *WebAccountCSV* entity includes the most accurate data about the *Full Names* attribute, you could prioritize this entity over *ContactCSV* by selecting *WebAccountCSV*. As a result, *WebAccountCSV* moves to first priority, while *ContactCSV* moves to second priority when pulling values for the *Full Name* attribute.

## Run your merge

Whether you manually merge attributes or let the system merge them, you can always run your merge. Select **Run** on the **Merge** page to start the process.

If you want to make additional changes and rerun the step, you can cancel an in-progress merge. Select **Stop** on the notification bar while the merging of records is in progress to stop the current run.

> [!div class="mx-imgBorder"]
> ![Data merge Save and Run](media/configure-data-merge-save-run.png "Data merge Save and Run")

After the **Merge is running** message disappears, merge has completed and resolved contradictions in your data according to the policies you defined. Your merged and unmerged attributes are included in your unified profile entity, while excluded attributes are not.

If this wasn't the first time you ran a merge successfully, all downstream processes, including enrichment, segmentation, and making measures will re-run automatically. You see the status of each downstream process by going to its page. After all downstream processes have been re-run, your customer profiles reflect any changes you made.

## Next Step

Configure [activities](pm-activities.md), [enrichment](pm-enrichment.md), or [relationships](pm-relationships.md) to gain more insights about your customers.

If this wasn't the first time you ran a merge successfully, all downstream processes, including enrichment, segmentation, and making measures will re-run automatically. You can see the status of each downstream process by going to its page. After all downstream processes have been re-run, your customer profiles will reflect any changes you made.
