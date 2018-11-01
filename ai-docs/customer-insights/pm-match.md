---
title: "Match| MicrosoftDocs"
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
# Match

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Once mapping is completed, you are ready to match your entities. Clicking the **Match tile** in the **Configuration page** will take you to the **Match page**:

![match-tile.png](media/match-tile.png)

Note that the Match phase requires at least two Mapped entities. If you have not mapped at least two entities, you can expect to receive the folloiwng message:
[match notification image1]

## The Match Phase
- As part of the Data Configuration process, **The Match Phase** enables you to specify how to combine your datasets into a unfied **Master Customer Dataset** that will be utilized later to unlock unique insights about your customers.

- If it's the first time you are going through the Match process, you should complete all the steps in this section:
  - 1.Specifying the first pair of entities that you want to Match (also called a *Match Pair*)
  - 2.Defining rule/s for the first Match Pair
  - 3.Running your first Match 
  - 4.(Optional) Reviewing and validating your first Match Pair
  - 5.(Optional) Making changes to your rule/s definition/s
  - 6.(Optional) Adding additional Matches as needed
  - 7.(Optional) Reviewing the order by which you chose to match your entities 
  
We will explore these steps in a sequential order. Prior to that we will give a quick introducion to the Map screen (can be skipped).

[replace with 11]
![match.png](media/match.png)

## Quick introduction to the Match Page
The **Match page** shown above includes two major sections: **Summary** and **Details**. We will first use the **Details** section to specify the Match Pair and setting it's rules (steps 1-2 as well as steps 5-6). Later we will use the **Summary** section to track the progress of our Match until completion as well as to validate the order by which we are matching our entities (validating step 3 and performing step 7). Lastly, above these components you will find three tiles and these will be used for step 4 above (for now there are no counts since no Match was executed).

## Step 1: Specifying a First Match Pair
Each **Match Pair** involves two entities that are unified into a single entity. Clicking the **Edit** button as shown below will enable you to create the first (as well as any future) Match Pair:

[15]

Upon clicking it, the following panel opens up:

[16]

Within this panel you will set the definitions for your first Match Pair: 
- **Start by selecting the first entity of your Match Pair** by clicking the left field (shown above in blue). 

**Important Note**: The entity that you will choose at this point will serve as the basis for your unified master data set. In other words, any future entities that you will be selected during the Match phase will be added to this entity (At the same time it doesn't mean that the unified entity will include all the data of your this entity). There are two considerations that can help you select your first entity:
    - First, what entity you consider to have the most reliable data?
    - Second, does the entity that you identified under considertion one has attributes that are also shared by other entities (those can be *Name*, *Phone*, *Email*, etc)? If not, you should continue to your second most reliable entity and so forth. 

- **Continue by selecting the second entity of your Match Pair** by clicking the right filed (shown above in red). 

**Note**: The considerations that were mentioned for your first selection can help you choose that entity as well (what is the second most reliable entity and does it include enough fields that are also shared by other mapped entities?)

- **Lastly**, hit **Save** and you will see that the **Description** now includes your first Match Pair. you can always **Delete** or **Edit** that match pair by clicking the **Edit** button as we did when we created that pair.
[]

## Step 2: Defining Rules for First Match Pair
For each of your match pairs you should define at least one **Rule**. **Match Rules** dictate the logic by which a specific pair of entities will be matched. In order to define rules for your first match, click the **Add Rule** as shown below:

[20]

Clicking **Add Rule** will open the following panel:

[21 plus numbers]
[maybe turn the following into a table?:]

Besides the rule's name, this panel enables you to specify all the ***Criteria*** for that role. Each Criteria is represented by a row that includes the following mandatory selections (going left to right):

- 1.**Attribute that will be used for matching from the first match-pair entities** (Name, Phone, Email or any other attribute)
- 2.**Normalization for first attribute:** Whether you want to normalize the values for the attribute you chose in (1). Various normalization options are available - from removing punctioation, to removing spaces, to many others. Note that for some attribute types (as defined under the **Types** column in the Map screen), a specific and optimal combination of normalizations will be automatically chosen for you (called **Semantic Normalization**). You can change this default setting to any of the other options.
- 3.**Attribute that will be used for matching from the second match-pair entities**
- 4.**Normalization for second attribute:** Same definitions as described under (3).
- 5.**The method that will be used for that criteria:** Selecting ***Exact*** will dictate that only matching records will be matched and selecting ***Fuzzy*** will dictate that records that are not 100% equal will also be matched. The threshold for Fuzzy matches will be selected next to it: You can define it as either **Low**, **Medium** or **High**. **High** fits cases where *Precision* is more important than *Reach* such as a financial service to a specific customer. **Low** fits cases where the opposite is true such as Marketing Campaign.

**Adding multiple criteria**:
If you wish to match your entities **only** if multiple conditions are met, you can do so by adding more criteria (which will be linked through an **AND** operator). To add criteria, simply click the **Plus button** as shown below in red. You can also remove criteria by clicking the same button (will show up as a **Minus button** for existing criteria as shown in blue):
[]

**Adding multiple rules**:
If each criteria reflects a condition around single attributes, then rules represent sets of conditions. Hence, if you believe that there different sets of attributes on the basis of which your two entities can be matched, you should add more rules at this point thorugh the **Add Rules** button that was shown earlier. Note that **order matters** when creating rules: The matching algorithem will try to match on the basis of your first rule (number as (1) in the **Description** section) and only then continue to the second rule (numbered as (2)) if no matches were identified with the first rule.

## Step 3: Running the First Match 
Now you are ready to run the matching that you have defined in steps 1-2. That can be done via the **Run** button as shown below:

[]

It's possible that the Matching algorithem will take some time to complete. Upon the completion of the matching you will get the following message and at this point you can **Save** the match and continue to the **Merge screen** or go through any of the optional steps (steps 4-7):

[]

Note that in the meantime there are two things you can do to track that progress of your match and evaluate the data behind it:

- **First, you can review the *Summary* section** (located above the **Description** section):

[]

This diagram visualizes the hierarchy by which your ingested entities are currently matched. Each of the entities is represented by a tile with the entity's name, the data source from which it was derived and number of records.

In addition to entities, the Suammry diagram includes the status of your match. Later we will cover the four possible status more in depth but for now we will describe the status of your current match which is called **Matching**:

[]

This status implies the matching process is currently in progress. Since it includes a percentage, you can track that progress.

- **Second, once the following message appears, you can review the *Master Data Set* that was created during the process:

[]

The **Entities** screen is where you can view the master data set. Upon clicking the **Entities tab** in the left side menu, you will be able to see that this new entity appears under the name **ConflationMatchEntity**:

[]

You can click on that entity and do a quick validation of the data that you are unifying:

[]

Within the table shown above, the left side (red) provides a preview of some of the records that were unified from the first match-pair entity. The right side (blue) provides the same view around the data that was broguht from the second entity. Lastly, the middle part 
(green) includes.. 

## Step 4 (Optional): Reviewing and Validating the First Match Pair
If you followed through step (3), then you already started to validate the quality of your first match. However, as part of the current and next steps, you will learn how to evaluate in depth this quality and improve it. There are a few things you can do:

- **First**, you can **gain first insights** by reviewing the tiles at the top of the page:
    - 1.The left tile shows the number of records that were successfully matched
    - 2.The center tile shows the number of records that were not successfully matched
    - 3.The right tile shows the number of customers that are included in the original two match-pair entities whether they were matched or not. This tile will provide you more context into the first number above - is that a relatively good or poor result?

Note that if you match more entities in the future these three numbers will present the **total** numbers of matched records, unmatched records, and customers across all your matchings taken together. When creating more matches, you can always view those numbers for a specific match by looking at this matche's row within the **Description** section. 

- **Second**, you can click the following button within the **Description** section in order to **view all your match pair records:**

[]

This screen presents all your match pair records. It is recommended to go through a part of it in order to validate that records were matched according to your expectations:

[]

- **Lastly**, you can **experiment with different threasholds around your criteria in order to identify the optimal threasholds**. In order to perform these experiments, follow the next few steps:
    - 1.Click the match pair rule you want to experiemnt with. In the example below, the user has identified the rule that is highlighted in red among the two rules that he has created:

   []

   - 2.Identify the criteria that you want to experiment with. Remember - each criteria is represented by one row in the panel below. Once identifyinf the criteria you want to experiment with, click the following button:
   
   []

   - 3.At this point the screen that you will see depends on whether you selected a **Fuzzy** or **Exact** match for that criteria. 
       - If you chose **Exact** for that criteria, you will see the following screen:
       
       []
       
       Here you can view the number of matched and unmatched records for that criteria (shown in red below). You can also view the records in the table section (shown in blue):
       
       - If you chose **Fuzzy** for that criteria, you will see the following screen:
       
       []
       
       This screen gives you a rich understanding around the effects of the three threshold levels. You can compare how many records will be matched under each of the threashold levels (shown below in red), as well as viewing the records under each option by clicking each of the tiles (shown in blue) and viewing the table section (shown in green):
       
       []
       
## Step 5 (Optional): Making Changes to the Rule/s Definitions
If you followed step (4), then at this point you should have a better understanding around the quality of your first match. At this point you can translate that understanding into a better match quality by reconfiguring some of your match parameters:

- **Changing the Match Pair entities**: That can be done by clicking the match row in the **Description** section and editing the match pair fields. Remember that the field to the left represents the entity that will be used as a basis for your end-state master entity and hence it should contain reliable data and some attributes that are shared by other entity or entities. 

- **Changing the order of your rules**: If you defined multiple rules, it might be worth changing their order in order to yeild a better match quality. That can be done by clicking the **Edit** button as shown earlier within the match row and subtituting the first rule's attributes with the second rule's attributes as shoen below:

[]

- **Editing your rules**: That includes several important changes that you should try as you optimize the match quality:
    - **Changing attributes for a criteria**: That can be done by reselecting new attributes within the criteria row
    - **Changing threashold for a criteria**: That can be quickly achieved via the threashold bar. In step (4) we covered how to get insight into the effects of the three threashold levels on your match quality.
    - **Changing normalization methods for a criteria**: That can be done by reselecting the normalization methods
    - **Changing from an *Exact* match to a *Fuzzy* match:** Doing so can lead to higher number of mathced records at the possible expence of lower accuracy. Doing the opposite might carry the opposie tradeoff (higher accuracy for lower number of matched records).
    
## Step 6 (Optional): Adding Additional Matches if Needed
Until this point you have created, ran, and evaluated one match. In many cases you will want at this point to bring data to your unified master data set from more entities. Prerequisite for doing so is that these additional entities were ingested through the **Get Data** page and mapped through the **Map** page.

In order to match a new entity with the unifed data set that you created in steps 1-2, click the **Add** button in the **Description** section:

[]

Then click the ? button in order to add another match pair:

[]

Note that upon clicking the ? button, a new row was created and the unified data set that you created in steps 1-2 now appears as one of the new match pair entities (highlighted in red below):

[]

In order to complete the creation of your second match, select the new entity that you want to match with your unified master entity (shown in blue below) and hit **Save**:

[]

Note that this point the new match will appear in the summary section too:

[]

However it has a **Rules Needed** status that implies that you havn't defined rules for that match pair yet (which again is mandatory in order to run the match). Hence at this point you should repeat steps 2-3 for that new match pair.


## Step 7 (Optional): Reviewing the Order by which multiple Matchings are Executed


- **Changing the order by which matches are executed:** That can be done by replacing a given row's values with another row's values. In the example above, in order to switch the order of the first match pair () and the second match pair (), we will need to replace the entities in the first match pair with those of the second match pair and vice versa. 

## Next Step
Once completed the Match process for at least one Match Pair, you are ready to resolve possible contradictions in your data by going through the **Merge** section, the third and last **Data Configuration** steps. 

