---
title: "Match| MicrosoftDocs"
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

# Match

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Once the *Map phase* is completed, you're ready to match your entities. Select the **Match** tile in the **Configure Data** page to get to the **Match** page:

// Replace 1
> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-tile.png "Match tile")

- Note that the Match phase requires at least two Mapped entities. If you have not mapped at least two entities, you can expect to receive a message which requires you to go back to the Map screen and Map at least two entities.

- If you did map at least two entities, you can expect to reach the following screen where you should click the **Set Order** button once you are ready to start the Match phase:

// missing 1

## The Match phase
The match phase enables you to specify how to combine your datasets into a unified **Customer Profile** dataset that will be utilized later to unlock unique insights about your customers.

If it's the first time you are going through the match process, you should complete all the mandatory steps in this section:
1. Specifying the order by which your mapped entities will be matched
2. Defining rules for the first match pair
3. Running your specified matches

In addition, you may want to complete the following steps as well:
4. (Optional) Reviewing and validating your matches
5. (Optional) Making changes to your Match Order and Rules' Definitions
  
Below, we will explore these steps in a sequential order. 

## Step One: Specifying the Match Order
Each **Match** involves two entities that are unified into a single entity while maintaining unique customer's records. In the example below, the user has selected three entities: *ContactCSV: TestData* as the **primary entity**, *WebAccountCSV: TestData* as **entity 2**, and *CallRecordSmall: TestData* as **entity 3**. The diagram above these selections helps explain how the match order will be executed: 
- **1st Match: First, the Primary entity will be matched with entity 2**
- **2nd Match: Then, the dataset resulted from the first match will be matched with entity 3**
- And so forth (in our example we made selections only for two matches but the system supports more than two)

  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-match-order-edit-page.png "Edit data match order")
  
> [!IMPORTANT]
> The entity that you will choose as your **primary entity** will serve as the basis for your unified master data set. In other words, any future entities that will be selected during the match phase will be added to this entity. At the same time it doesn't mean that the unified entity will include **all** of the data included in this entity.

>There are two considerations that can help you select your primary entity:
> 1. What entity do you consider having the most complete and reliable data about your customers?
> 2. Does the entity that you identified under consideration (1) has attributes that are also shared by other entities (Name, Phone, Email, etc)? If not, you might consider to choose your second most reliable entity.

> [!NOTE]
> Considerations for your first selection can help you choose your **entity 2** as well. Among your ingested (and mapped) entities, what entity do you consider to have the second most reliable and complete data? Moreover, does it include at least one field that is shared by the primary entity as well as possibly additional fields that are shared by other ingested entities?

You can always remove entities from your Match Order by selecting the button that is shown in blue below. Lastly, click **Save** to save your Match order as shown in red:

// missing 2

## Step Two: Defining rules for your first match pair
Once completing step one, you can expect to reach the Match screen that is shown below and which includes your defined matches (in the example below the user specified two matches). Note that the tiles at the top of the screen will be empty until we will run our match order in step 3. These will be used for validation as explained in step 4.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-need-rules.png "Need rules")

Moreover, the warning sign (shown in red above) implies that we didn't define **at least one match rule** for our match pair which is mandatory for each of our match pairs. Match rules dictate the logic by which a specific pair of entities will be matched. In order to define your first rule, open the **Rule Definition Panel** by clicking the corresponding match row in the matches table, and then clicking the **create new rule** button: 

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-new-rule.png "Create new rule")

That will open the following **rule panel**:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-new-rule-condition.png "Create new rule and conditions")

Besides the rule's name, this panel enables you to specify all the ***Conditions*** for that role. Each Condition is represented by two rows that include the following mandatory selections:

1. **Attribute that will be used for matching from the first match pair entity**: Name, Phone, Email Address, etc. 

[IMPORTANT!]
> You should avoid matching on the basis of activity-type attributes. In other words, if an attribute seems to be an activity, then it might be a poor criteria to match by.  

2. **Attribute that will be used for matching from the second match pair entity**.

3. **Normalization method**: Various normalization options are available for the attributes chosen in fields (1) and (2) - from removing punctuation, to removing spaces, to many others. Note that for some attribute types, a specific and possibly optimal combination of normalizations will be automatically chosen for you. This option is called **Semantic Normalization** in the drop down and you can change this default selection to any of the other options:

4. **The level of precision that will be used for that condition:** 
- Selecting ***Exact*** on the left side of the scale will dictate that only matching records will be matched. 

[IMPORTANT!]
> Choosing Exact Match on the basis of the same AttributeId type (for example AccountId, ContactId, etc) will not lead to optimal result. While you may want to link the two entities through a relationship (visit the Relationships section in order to review), the match process should be executed on the basis of other attributes. 

- Selecting one of the other levels will dictate that records that are not 100% identical will also be matched. **High** fits cases where precision is more important than reach such as a financial service to a specific customer. **Low** fits cases where the opposite is true such as a marketing campaign. The **Medium*** level servs as a middle-ground option. 

### Adding multiple conditions
If you wish to match your entities **only** if multiple conditions are met, you can do so by adding more conditions which will be linked through an **AND** operator. Simply click the **Add Condition** button as shown below in blue. You can also remove conditions by selecting the button that is highlighted in red.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-new-rule-add-condition.png "Add condition")

For the purpose of this section we will limit our match rule to only one condition.

### Adding multiple rules
If each condition applies to a single pair of attributes, then rules represent sets of one or more conditions. If you believe that your entities can be matched on the basis of different sets of attributes, you should add more rules using the **Add Rules** button. Note that when creating rules order matters: The matching algorithm will try to match on the basis of your first rule (represented by the first row in the table shown in red below) and continue to the second rule (represented by the second row) only if no matches were identified under the first rule: 

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-new-rule-priority.png "New rule priority")

For the purpose of this section we will stay with only one rule.

## Step Three: Running your Specified Match Order
Now you are ready to run the match order that you have defined in steps (1) and (2). This can be done by clicking **Save** and then **Run** as shown below. Next to these buttons there is a **Discard** button that enables you to delete the definitions of your match (shown in red).

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-commands.png "Edit rule add new criteria")

It's possible that the matching algorithm will take some time to complete. While running, you can expect to see the following status diagram:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-running.png "Data match running")

**While it's not possible to use any of the match screen functionalities until the match process completes, it's possible to visit other product modules through the left navigation menu** (for example you may want to utilize this time to define relationships through the Relationships screen or activities via the Activities screen. Visit those sections to learn more).

Also note that above the diagram there is a **Matching records** notification as long as the Match algorithem is running. Upon the completion of the process, the match screen will become available again and the **Matching records** message will disappear. 

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-run-complete.png "Data match run is complete")

As mentioned in step one, the first match results in the creation of a unified master entity while all subsequent matches result in the expansion of that entity. Hence, upon the completion of the matching process a preview of the unified customer entity can be viewed by clicking the folloiwng button:

> [!div class="mx-imgBorder"] 
> ![](media/match-conflation-match-pairs.png "Conflation Match Pairs")

Which will open the Customer Profile Preview window: 

> [!div class="mx-imgBorder"] 
> ![](media/match-conflation-match-pairs-download.png "Conflation Match Pairs download")

Note that:
- The column shown above in blue reflects for each of your recods how certain it is that it was accurately matched (confidence score)
- The rest of the columns present the data that was taken from the two original entities. Columns to the left of the highlighted column present data that was taken from the first match pair entity, while columns to the right present data taken from the second match pair entity. 
- You can also view the customer profile entity within the **Entities screen.**
- Lastly, as shown in red, you can also download the customer profile dataset. 

At this point you can either continue to the **Merge** page or go through any of the optional steps in this section (Steps 4-5). However, it's recommended to go through at least a portion of step 4 in order to validate the quality of your match which, in turn, can help you decide whether to continue to Merge or reconfigure your match definitions.

## Step Four (optional): Reviewing and Validating your Match Pairs
Here you will learn how to evaluate in depth your match pairs qualities and improve it. There are a few things you can do.

**First**, you can gain first insights by reviewing the tiles at the top of the page (shown in red below):

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-results.png "Data match results")

1. The left tile shows the number of **unique profiles** the system had identified.
2. The right tile shows the number of matches, in total, that were completed accross all of your match pairs. This tile will provide you more context into the first number - is that a relatively good or poor result?

**Second**, you can assess the results of each match pair as shown in blue above - viewing number of records that came from this match pair entities side by side with the percentage of successfully matched records.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-view-rule-level.png "View at the rule level")

**Third,** you can view the percentage of successfully matched records at the Rule-level (shown in red above). Moreover, by clicking the button that is shown in blue you can view all these records (again, on the rule-level). The following window examplifies the preview you can expect to see:

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-match-preview.png "Match preview")

It is recommended to go through at least a part of it in order to validate that records were matched according to your expectations.

**Lastly**, you can experiment with different thresholds around your conditions in order to identify the optimal thresholds. In order to perform these experiments, follow the next few steps.

1. Select the **Three Dots Icon** for the match pair rule that you want to experiment with (an example is shown in red below). Then, click **Edit** as also shown in red:

  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-match-pair-edit.png "Edit match pair")

2. Identify the condition that you want to experiment with. Remember, each criterion is represented by one row in the panel below. Once you've identified it, select the following:
   
// Missing 3

3. At this point the page that you see depends on the match level you have selected for that condition. 

  If you chose **Exact** for that condition, you will see the following page.

  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-match-criteria-preview.png "Match criteria preview")

  Here you can view the number of matched and unmatched records for that condition (shown in red below). You can also view the records in the table section (shown in blue).
       
  If you chose one of the other levels for that condition, you will see the following page.
       
  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-match-fuzzy-criteria.png "Match criteria preview")
     
This page gives you a rich understanding around the effects of the three threshold levels. You can compare how many records will be matched under each of the threshold levels (shown below in red), as well as viewing the records under each option. Select each of the tiles (shown in blue) and view the table section (shown in green).
       
## Step Five (optional): Making Changes to Optimize your Matches
If you followed Step Four, then at this point you should have a better understanding around the quality of your first match. At this point you can translate that understanding into a better match quality by reconfiguring some of your match parameters.

- **Changing the Match Order**: That can be done by selecting the **Edit** button shown below and editing the match order fields:

  > [!div class="mx-imgBorder"] 
  > ![](media/configure-data-match-order-edit.png "Edit data match order")

- **Changing the order of your rules**: If you defined multiple rules, it might be worth changing their order in order to yield a better match quality. That can be done by selecting **Edit** as shown earlier within the match row and substituting the first rule's attributes with the second rule's attributes.

- **Editing your rules**: This includes several important changes that you should try as you optimize the match quality.
    - **Changing attributes for a condition**: This can be done by reselecting new attributes within the specific condition row.
    - **Changing threshold for a condition**: This can be quickly achieved via the threshold bar. In Step Four we covered how to get insight into the effects of the three threshold levels on your match quality.
    - **Changing normalization method for a condition**: This can be done by reselecting the normalization methods.
    - **Changing from an *Exact* match to a *Fuzzy* match:** Doing so can lead to a higher number of matched records at the possible expense of lower accuracy. Doing the opposite might carry the opposite tradeoff - higher accuracy for a lower number of matched records.
    
## Next Step
Once you've completed the match process for at least one match pair, you are ready to resolve possible contradictions in your data by going through the **Merge** section, the third and last **Data Configuration** step. 

