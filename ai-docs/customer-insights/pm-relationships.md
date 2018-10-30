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

**Beside entities, in customer 360 you can also define Relationships between entities.** Relationships help to define the data graph based on entities ingested from different data sources as well as relate the data graph to master customer profile based on intelligent matching done by AI/ML algorithms. These entities and relationships-based data graph are useful for segmentation and other analytical purposes. There are 2 types of relationships:

- **System relationships:** These are created by system automatically and cannot be edited.
- **Custom relationships:** These are created by user during configuration and can be edited.

**During the Match and Merge process system relationships are already created behind the scenes based on intelligent matching.** These system relationships are created to relate master customer entity with match rule entities. One relationship is created per master customer entity and match rule entity combination. These relationships help relate the master customer record with corresponding match entity records. Diagram below exemplifies the creation of 3 system relationships when 3 match entities are merged to create master customer entity:

> [!div class="mx-imgBorder"] 
> ![](media/relationships-entities-merge.png "Relationship creation")

- **CustomerToContact relationship** was created between the Customer entity and the Contact entity and is based on match executed between Customer entity and Contact entity. Customer entity gets the key field Contact_contactId to relate to Contact entity key field contactId.
- **CustomerToAccount relationship** was created between the Customer entity and the Account entity is and is based on match executed between Customer entity and Account entity. Customer entity gets the key field Account_accountId to relate to Account entity key field accountId.
- **CustomerToWebAccount relationship** was created between the Customer entity and the WebAccount entity and is based on match executed between Customer entity and WebAccount entity. Customer entity gets the key field WebAccount_webaccountId to relate to WebAccount entity key field webaccountId.
In addition, you can define Custom Relationships by using the Relationships link in the Configure area as shown below:

> [!div class="mx-imgBorder"] 
> ![](media/relationships-custom.png "Custom relationships")

This page provides actions to add, edit or delete relationships. Each Relationships has 2 key parts:
- **Source Entity:** This represents the many end of relationship. In relational schema terminology, this represents the entity that holds the foreign key.
- **Target Entity:** This represents the one end of relationship. In relational schema terminology, this represents the entity that source entity’s foreign key points to.

To create a relationship, you need to provide the following information:

> [!div class="mx-imgBorder"] 
> ![](media/relationships-add.png "Add a relationship")

- **Relationship Name:** This is the name that you, as a user, assign to that relationship. Each relationship name must be unique. This should provide a useful name to reflect the purpose of the relationship e.g. AccountWebLogs.
- **Description:** Optional information to describe the relationship.
- **Source Details:**
    - **Entity:** That is the name of the entity that is used as a source in the relationship e.g WebLog.
    - **Cardinality:** This represents the cardinality of the source entity records. For example, many means that multiple Weblog records are related to one WebAccount.
    - **Source lookup/link field:** This field represent the foreign key field in source entity e.g. WebLog has the accountId foreign key field.
- **Target Details:**
    - **Entity:** That is the name of the entity that is used as a target in the relationship e.g. WebAccount 
    - **Target Cardinality:** This represents the cardinality of the target entity records. For example, one means that multiple Weblog records are related to one WebAccount.
    - **Target key field:** This field represent the key field of target entity e.g. WebAccount has the accountId key field.
For now, only Many to One and One to One type relationships are supported. Many to Many type relationships can be created using two Many to One relationship using a link entity.

System and Custom relationships are used in Segment Builder to navigate from entity on one end of the relationship to entity on the other end of the relationship as you define conditions to filter customers based on the data graph ingested entities from data sources. For more information, on how to use relationships in Segment Builder, refer to documentation on creating segments.






> [!div class="mx-imgBorder"] 
> ![](media/add-relationships.png "Add relationships")
