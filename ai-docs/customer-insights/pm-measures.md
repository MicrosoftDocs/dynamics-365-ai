
---
title: "Measures| MicrosoftDocs"
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

## Measures

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The **Measures screen** enables you to define all the KPIs that best reflect your specific business domain and goals.                     Once defined, you can benefit from your measures in a verity of ways. For example:
- Consume on your Homepage (Dashboard) Screen 
- View for a specific customer as part of the **Customer Card** (visit the *Customer Card Section* to learn more) 
- Use to define your segment by, using the Segment Builder Screen

### Step1: Choosing between Three Measure Types
There are two early decisions you should make with regard to your desired measure. These decisions will help you choose between the three options that are available to you when you click the **New Measure** button:

// 1

// 2

- First, you should decide whether you wish to:
  - Save your measure as an attribute within one of your existing entities - than you should choose the **Profile Attribute** option 
  - Or create a new entitiy around your measure 
  
- 2.If decided to save the measure as an entity, you should also decide whether to:
  - Create the measure on the basis of field/s from the Customer Profile entity - which corresponds to the **Profile Measure** option
  - Or create it on the basis of another ingested entity - which corresponds to the **Business Measure**
  
Also note that your choice at this point will affect the number of dimensions supported for your measure. **Dimension** is... You will choose your dimensions in step 4 when we will summarize our measure. 
- Profile attribute and Profile Measure are limited to a single dimension
- Business Measure, on the other end, supports multiple dimensions 

In the next three sub-sections we will explore the steps you should complete in order to define your measure. 

### Step2: Choosing the Base Entity
Upon choosing one of the options, you can expect to reach the **Measure Creation Panel**.

**Panel you can expect to see upon selecting the *Business Measure* option**:

// 3

**Name** (mandatory): Upon completing the configuration of your measure, it will show up in the Measures screen as a saved measure that you can edit. Within the measures screen, your saved measure will carry the name you define under the **Name** field in this panel.
**Display Name** (optional): As mentioned earlier, your measure will also be added as an attribute or be saved a new entity. In both cases, the measure will carry the name you define under the **Display Name** field in this panel.
**Starting Entity** (mandatory): Here you should choose the entity on the basis of which you wish to construct your measure. If you wish to include in your measure fields from multiple entities, choose at this point any of these entities.  

**Panel you can expect to see upon selecting the *Profile Measure* and *Profile Attribute* options**:

// 4

This panel is the same panel we explored under the previous options except for one difference: **The Customer Profile entity will automatically be selected as your starting entitiy**. Morvoer, this default selection can't be changed. 

### Step3: Choosing Related Entities
Once completing step one, you can expect to see the following screen:

// 5

Within this screen we will complete steps 3-5 in the Measure definition process.

First you should decide whether additional entities are needed as part of your measure definition. One example might be creating an expression that will be based on attributes from two or more different entities (we will explore that use case in step 4). 

In order to choose additional entities, simply click the **Add new entity** button and pick the entitites of your interest:

// 6

**Note**: You can only select entities which have relationships to your base entity. If you havn't define relationships yet, make sure to read the **Relationships** section.

### Step4: Calculating a Variable
Ths step is accessable via the **Add new variable** button:

// 7

Upon clicking it, you should reach the **Variable Definition Panel**:

// 8

Let's explore the steps you should complete in this panel:
1. Giving you variable a name: You can give your variable a recognizable name
2. Clicking the Expression area:

// 9

3. Choosing a field from the fields shown to the right:

// 10

4. Typing an expression in the expression area while choosing more fields (**Note**: At this point we only support arithmathic expressions)

// 11

5. Clicking **Done**.

### Step5: Summarizing
In this final step we will decide how to aggragate our measure. 

**Step1:** Click **Add new dimension**: That will open the *Summarize* type of aggragate.  ...
If you do wish to have that aggragate, those are the selections you should fill:
**Summarize**
**Entity**
**Field**
**As**
**Display Name**

**Step2 (optional):**: Add more **summarize** dimensions by clicking **Add new measure**

**Step 3**: Click **Add new Dimension**: That will open the *Group by* type of aggragate.  ....
If you do wish to have this aggragate, those are the selections you should fill:
**Group by**
**Field**
**Bucket**
**As**
**Display Name**

### Viewing and Editing your Measures 

### Next Step

