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

It's possible that the Matching algorithem will take some time to complete. In the meantime there are two things you can do to track that progress and evaluate the data that you are matching.

- **First, you can review the *Summary* section**:

[]

This diagram visualizes the hierarchy by which your ingested entities are currently matched. Each of the entities is represented by a tile with the entity's name, the data source from which it was derived and number of records.
In addition to entities, the Suammry diagram includes three types of status for your matches. Those are stated on top of the links that connect each matching pair. 

[]

- In the example above, all these links have the same status: **Rules Needed**. This status implies that no rules were defined for the match pair. As stated earlier, **at least one rule *must* be added to each of the matchings**.
- Once rules were defined for a given match pair, it's status will turn to **Ready to Run**. As we will see, running a match is also available within the **Details** section. 
- **Matching** is the third status you can see for a given match pair. This status implies that the matching process is currently under progress (reflected as a percentage).   
- **Complete** is the forth and last status you can see for a given match pair and it reflects the completion of the matching process both for this matching and for all the matchings that precede it. In the example shown below


## Step 4 (Optional): Reviewing and Validating the First Match Pair

## Step 5 (Optional): Making Changes to the Rule/s Definitions

## Step 6 (Optional): Adding Additional Matches as Needed

## Step 7 (Optional): Reviewing the Order by Which We Chose to Match Our Entities
- **Changing the order by which matches are executed:** That can be done by replacing a given row's values with another row's values. In the example above, in order to switch the order of the first match pair () and the second match pair (), we will need to replace the entities in the first match pair with those of the second match pair and vice versa. 

## Next Step
Once completed the Match process for at least one Match Pair, you are ready to resolve possible contradictions in your data by going through the **Merge** section, the third and last **Data Configuration** steps. 

## Summary Section
This diagram visualizes the hirarchy by which your ingested entities are currently matched. Each of the entities is represented by a tile with the entity's name, the datasource from which it was dervied, number of records, end possibility to view those records by clicking the button at the bottom-right corenr of the tile.                                

To examplify the logic that is captured in the **Summary** part, the following matching sequence is reflected in the diagram below:
- First, *Sales Data* from *Salesforce* will be matched with *Sales Data* from *Dynamics 365*
- Then, the matched dataset that resulted from step one will be matched with *Survey Data* from *Salesforce*
- Then, the matched dataset from step two will be matched with *Solication Data* from *Salesforce*
- Lastly, the matched dataset from step three, will be matched with another *Sales Data* dataset from *Salesforce*
    
[13]

In addition to entities, the Suammry diagram includes three types of status for the different matchings. Those are stated on top of the links that connect each matching pair. 
- In the example above, all these links have the same status: **Rules Needed**. This status implies that no rules were defined for the match pair. As we will see, **at least one rule *must* be added to each of the matchings** and it can be done in the **Details** section
- Once rules were defined for a given match pair, it's status will turn to **Ready to Run**. As we will see, running a match is also available within the **Details** section. 
- **Matching** is the third status you can see for a given match pair. This status implies that the matching process is currently under progress (reflected as a percentage).   
- **Complete** is the forth and last status you can see for a given match pair and it reflects the completion of the matching process both for this matching and for all the matchings that precede it. In the example shown below, the first two matchings were completed while the third matching is under progress:

[14]



### Details Section
This section captures your matchings in a table. Let's explore the **Details** table fields, going left to right:

[17]

   - The first column specifies the order by which the matchings will take place (reflecting the same sequence as in the summary part)
   - The next two columns specify the specific match pair members, whether these are single entities (highlighted in blue in the example above), or datasets resulted from prior matchings (highlighted in red in the example above).
   - The next two columns specify the number of matched and unmatched records **for that specific matching** 
   - The last column includes a status icon: A **warning sign** will change into a **checked circle sign** once a match pair is in **Complete** status

Next to these fields you will find a **three dots icon**:

[18]

Clicking it will enable you to perform the following actions:
- **Running a match pair**. Clicking **Run** in one of the rows will run only the matching that is represented in that row. For running all your match pairs at the same time, go to the bottom of the Match screen and hit the **Run All** button:

[19]

- **Adding and Editing Match Pair Rules:** Clicking **Edit** will open the **Edit Match Rule** pop-up window:

[20]

Besides the role name, this panel enables you to specify all the ***Criteria*** for that role. Each Criteria is represented by a row that includes (going left to right):

[21 plus numbers]
[turn into a table:?] 

- The attribute that will be used for matching within the first match-pair entity
- The attribute that will be used for matching within the second match-pair entity
- The method that will be used for that criteria: Selecting ***Exact*** will dictate that only matching records will be matched and selecting ***Fuzzy*** will dictate that records that are not 100% equal will also be matched. The threshold for Fuzzy matches will be selected next to it: You can define it as either *Low*, *Medium* or *High*.
- An either **OR** or **AND** operator where:
  - **AND** states that the criteria will be executed together** with the next criteria
  - **OR** states that either this or the next criteria should be executed

![match-edit-rule.png](media/match-edit-rule.png)
