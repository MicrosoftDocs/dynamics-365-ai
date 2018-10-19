---
title: "Relationships| MicrosoftDocs"
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
# Relationships

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Beside entities, in customer 360 you can also define and utilise *Relationships* between entities. Those are useful for segmentation and other purposes. Note that during the **Merge** process some relationships were already created behind the scenes. Those are called **System Relationships** and they are used to dictate the way segmentation will be applied to your specific data. For illustration, the digram below examplifies the creation of three system relationships:
- Relationship was created between the **Customer** entity and the **Contact** entity due to a merge that was executed between Customer_ContactID and Contact_ContactID.
- A second relationship was created between the **Customer** entity and the **Account** entity due to a merge that was executed between Customer_AccountID and Account_AccountID.
- A third relationship was created between the **Customer** entity and the **Web** entity due to a merge that was executed between Customer_WebID and Web_WebID.

[]

In addition, you can define **Customzied Relationships** by using the **Relationships Page** that is shown below. This screen includes five columns and we will explore these from left to right:

- **Relationship Name**: That is the name that you, as a user, assign to that relationship so it will be considered as an entity
- **Source Entity**: That is the name of the entity that is used as a source in that unidirectional/bidirectional relationship 
- **Source Cardinality**: Number that represents the number of nodes of the source entity. For example, if the number is 2 it means that two sources lead to one/more target entities in that relationship.
- **Target Entity**: That is the name of the entity that is used as a target in that relationship
- **Target Cardinality**: Number that represents the number of nodes of the target entity. For example, if the number is 1 it means that the source entity/entities lead to only one target entity.
- Lastly, the available actions on that page include adding a new relationship or deleting a relationship as highlighted below

> [!div class="mx-imgBorder"] 
> ![](media/add-relationships.png "Add relationships")
