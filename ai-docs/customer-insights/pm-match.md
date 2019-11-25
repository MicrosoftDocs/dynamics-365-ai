---
title: "Match | Microsoft Docs"
description: Complete the matching phase to get a unified customer profile in Dynamics 365 Customer Insights
ms.date: 11/25/2019
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Match

After completing the map phase, you're ready to match your entities. The match phase lets you specify how to combine your datasets into a unified customer profile dataset, which will be used to gain unique insights about your customers. The match phase requires at least [two mapped entities](pm-map.md).

## Specify the match order

Go to **Unify** > **Match** and select **Set order** to start the match phase.

<!--remove example since it's not consistent?-->

Each match involves two entities that are unified into a single entity, while persisting each unique customer record. In the following example, we selected three entities: **ContactCSV: TestData** as the **Primary** entity, **WebAccountCSV: TestData** as **Entity 2**, and **CallRecordSmall: TestData** as **Entity 3**. The diagram above the selections illustrates how the match order will be executed.

> [!div class="mx-imgBorder"]
> ![Edit the data match order](media/configure-data-match-order-edit-page.png "Edit the data match order")
  
First, the **Primary** entity is matched with **Entity 2**. Then, the dataset that results from the first match is matched with **Entity 3**.
In this example, we only selected two matches. However, the system supports more matches.

> [!IMPORTANT]
> The entity that you choose as your **Primary** entity will serve as the basis for your unified master dataset. Additional entities that are selected during the match phase will be added to this entity. At the same time, this doesn't mean that the unified entity will include *all* of the data included in this entity.
>
> There are two considerations that can help you choose the hierarchy of your entities:
>
> - What entity do you consider having the most complete and reliable data about your customers?
> - Does the entity that you just identified have attributes that are also shared by other entities (for example, name, phone number, or email address)? If not, choose your second most reliable entity.

Select **Done** to save your match order.

## Define rules for your first match pair

After specifying the match order, you'll get back to the **Match** page which now lists the defined matches. The tiles at the top of the screen will be empty until you run your match order the next step.

> [!div class="mx-imgBorder"]
> ![Define rules](media/configure-data-match-need-rules.png "Define rules")

The **Needs Rules** warning suggests that no match rule is defined for a match pair. Match rules specify the logic by which a specific pair of entities will be matched.

1. To define your first rule, open the **Rule Definition** pane by selecting the corresponding match row in the matches table (1) and then selecting **Create new rule** (2).

   > [!div class="mx-imgBorder"]
   > ![Create new rule](media/configure-data-match-new-rule2.png "Create new rule")

2. In the **Edit Rule** pane, configure the conditions for that rule. Each condition is represented by two rows that include mandatory selections.

   > [!div class="mx-imgBorder"]
   > ![New rule pane](media/configure-data-match-new-rule-condition.png "New rule pane")

   1) An attribute that will be used for matching from the first match pair entity (for example, name, phone, or email address). Choose an attribute that is likely unique to the customer, and similar information can be found in other entities.

   > [!TIP]
   > Avoid matching on the basis of activity-type attributes. In other words, if an attribute seems to be an activity, then it might be a poor criteria to match by.  

   2) An attribute that will be used for matching from the second match pair entity.

   3) **Normalization method**: Various normalization options are available for the selected attributes. For example, removing punctuation or removing spaces

   For Organization name normalization (Preview), you can also select **Type (Phone, Name, Organization)**

   > [!div class="mx-imgBorder"]
   > ![Normalization-B2B](media/match-normalization-b2b.png "Normalization-B2B")

   4) The level of precision that will be used for this condition. Select **Exact** to only match records that that match 100 percent. Select one of the other levels to match records that are not 100 percent identical. You can also use the slider to define the percentage that records need to match. Values on the slider are between 0 and 1. So 0.64 represents 64 percent.

3. Select **Done** so save the rule.

### Add multiple conditions

If you want to match your entities only if multiple conditions are met, you can do so by adding more conditions that are linked through an AND operator.

1. In the **Edit rule** pane, select **Add condition**. You can also delete conditions by selecting the remove button next to an existing condition.

2. Select **Done** so save the rule.

## Add multiple rules

If each condition applies to a single pair of attributes, then rules represent sets of one or more conditions. To have your entities matched on the basis of different sets of attributes, you can add more rules.

1. In Customer Insights, go the the **Match** page.

2. Select the entity your want to update and select **Add rules**.

3. Follow the procedure as outlined in [Define rules for your first match pair](#define-rules-for-your-first-match-pair).

> [!NOTE]
> The rule order matters. The matching algorithm tries to match on the basis of your first rule and continues to the second rule only if no matches were identified under the first rule.

## Run your match order

After defining the match rules, you can run the match order. On the **Match** page, select **Run** to start the process. The matching algorithm might take some time to complete. You can't change properties on the **Match** page until the match process completes. You can find the unified customer profile entity which was created on the **Entities** page. Your unified customer entity is called **ConflationMatchPairs: Customer 360**.

When the match process is complete, the **Matching records** message disappears and you can use all functionality of the page again.

The first match process results in the creation of a unified master entity. All subsequent match runs result in the expansion of that entity.

To see a preview of the unified customer entity after running the match process, select **View last run**.

> [!div class="mx-imgBorder"]
> ![View last run](media/match-conflation-match-pairs.png "View last run")

The preview shows details about the matches and how confident the system is about the accuracy of the match. Select **Download** to in the preview to download the customer profile dataset.

## Review and validate your matches

Evaluate the quality of your match pairs and refine it:

- On the **Match** page, you'll find two tiles showing initial insights about your data.

  - **Unique customers** shows the number of unique profiles that the system identified.
  - **Matched records** shows the number of matches across all of your match pairs.

- In the **Match order** table, you can assess the results of each match pair by comparing the number of records that came from this match-pair entity side by side with the percentage of successfully matched records.

- In the **Rules** section of an entity in the **Match order** table, you'll find the percentage of successfully matched records at the rule level. By selecting the table symbol next to a rule, you can view all these records on the rule level. We recommend that you review a subset of the records to validate that they were matched correctly.

- Experiment with different precision thresholds around your conditions to identify the optimal value.

  1. Select the ellipsis (...) for the match pair rule that you want to experiment with and select **Edit**.

  2. Select the condition that you want to experiment with. Each criterion is represented by one row in the **Match rule** pane.

  3. The **Criteria preview** page that you see depends on the precision level you have selected for a condition. Find the number of matched and unmatched records for the selected condition.

     Get a rich understanding of the effects of different threshold levels. You can compare how many records will be matched under each of the threshold levels, as well as viewing the records under each option. Select each of the tiles and review the data in the table section.

## Optimize your matches

After following the guidance in the previous section you should have a better understanding of the quality of you match runs. Increase the quality by reconfiguring some of your match parameters:

- **Change the match order** by selecting **Edit** and change the match order fields.

  > [!div class="mx-imgBorder"]
  > ![Edit data match order](media/configure-data-match-order-edit.png "Edit data match order")

- **Change the order of your rules** if you defined multiple rules. You can reorder the match rules by selecting the **Move Up** and **Move Down** options in the match rules grid.

  > [!div class="mx-imgBorder"]
  > ![Change rule order](media/configure-data-change-rule-order.png "Change rule order")

- **Duplicate your rules** if you defined a match rule and would like to create a similar rule with modifications by selecting the **Duplicate** option.

  > [!div class="mx-imgBorder"]
  > ![Duplicate a rule](media/configure-data-duplicate-rule.png "Duplicate a rule")

- **Edit your rules** by selecting the **Edit** symbol. You can apply the following changes:

  - Change attributes for a condition: Select new attributes within the specific condition row.
  - Change the threshold for a condition: Adjust the precision slider.
  - Change the normalization method for a condition: Update the normalization method.

## Specify your custom match records regardless of the rules

To specify the conditions that certain records always match and/or certain records never match based, you can upload those rules in bulk to the match process.

1. Select the **Custom match** option on the **Match order** screen.

   > [!div class="mx-imgBorder"]
   > ![Create a custom match](media/custom-match-create.png "Create a custom match")

2. If you have no uploaded entities, you will see a new **Custom match** dialog box which requires you to fill in some details. If you've done this before, proceed to step 8.

   > [!div class="mx-imgBorder"]
   > ![New custom match dialog box](media/custom-match-new-dialog-box.png "New custom match dialog box")

3. Select **Fill in the template**. This downloads a template file that can be used to specify which records from which entities should always match and/or never match. You'll need to separately fill in the always match records and never match records in two different files.

4. The template contains fields to specify the entity and the entity primary key values to be used in the custom match, for example, if you want primary key 12345 from Sales entity to always match with primary key 34567 from Contact entity, you need to specify as follows:
    - Entity1: Sales
    - Entity1Key: 12345
    - Entity2: Contact
    - Entity2Key: 34567

   The same template file can specify custom match records from multiple entities.

5. After adding all the overrides you want to apply, save the template file.

6. In Customer Insights, go to **Data sources** and ingest the template files as new entities. Once ingested, you can use them to specify the Match configuration.

7. After uploading the files and entities are available, select the **Custom match** option again and you'll see options to specify the entities you want to include. Select the required entities from the drop down menu. Selecting an entity is not compulsory if you choose to skip either always match and/or never match.

   > [!div class="mx-imgBorder"]
   > ![Custom match overrides](media/custom-match-overrides.png "Custom match overrides")

8. Select the entities you want to use for **Always match** and **Never match**, select **Done**.

9. Select **Save** on the **Match** page for the custom match configuration you just set up.

10. Select **Run** on the **Match** page to start the matching process and the custom match configuration will be taken in to effect, and any system matched rules are overridden by the configuration set.

11. Once the matching is complete, you can verify the **ConflationMatchPair** entity to confirm that the overrides are actually applied in the conflation matches.

## Next Step

Once you've completed the match process for at least one match pair, you are ready to resolve possible contradictions in your data by going through the [**Merge**](pm-merge.md) topic.
