---
title: "Relationships| MicrosoftDocs"
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
# Relationships

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## What Relationships are useful for?
In Customer 360 you can define **relationships** between entities. As we will see within the **segments** section, these relationships are useful for segmentation. In the future they will be used for additional analytical purposes within Customer 360.

> [!div class="mx-imgBorder"] 
> ![](media/configure-data-relationships-tile.png "Relationships tile")

There are two types of relationships:

- **System relationships:** These are created by the system automatically and cannot be edited.
- **Custom relationships:** These are created by the user during configuration and can be edited.

During the match and merge processes, system relationships are created behind the scenes based on intelligent matching. These relationships help relate the Customer Profile records with other, corresponding entities' records. The diagram below exemplifies the creation of three system relationships when the customer entity is matched with additional entities to produce the final Customer Profile entity:

> [!div class="mx-imgBorder"] 
> ![](media/relationships-entities-merge.png "Relationship creation")

- **CustomerToContact relationship** was created between the **Customer entity and the Contact entity**. The Customer entity gets the key field **Contact_contactId** to relate to the Contact entity key field **contactId**.
- **CustomerToAccount relationship** was created between the **Customer entity and the Account entity**. The Customer entity gets the key field **Account_accountId** to relate to Account entity key field **accountId.**
- **CustomerToWebAccount relationship** was created between the **Customer entity and the WebAccount entity**. The Customer entity gets the key field **WebAccount_webaccountId** to relate to WebAccount entity key field **webaccountId.**

## Using the Relationships Screen to Add and Edit Entities
In addition, you can use the **Relationships Screen** to define custom relationships as shown below (accessable through the **Relationships** tab on the left side menu):

> [!div class="mx-imgBorder"] 
> ![](media/relationships-custom.png "Custom relationships")

Each relationship has two key parts:
- **Source Entity:** This represents the **many ends** of the relationship. In relational schema terminology, **this represents the entity that holds the foreign key.**
- **Target Entity:** This represents the **one end** of the relationship. In relational schema terminology, **this represents the entity that the source entity’s foreign key points to.**

To create a relationship, first click **Add Relationship*:

> [!div class="mx-imgBorder"] 
> ![](media/add-relationships.png "Add relationships")

Then you need to provide the following information in the Relationship panel:

> [!div class="mx-imgBorder"] 
> ![](media/relationships-add.png "Add a relationship")

- **Relationship Name:** The name that you, as a user, assign to that relationship. Each relationship name must be unique. This should provide a useful name to reflect the purpose of the relationship (for example, AccountWebLogs).
- **Description:** Optional information to describe the relationship.
    - **Source Entity:** The name of the entity that is used as a source in the relationship (for example, WebLog).
    - **Cardinality:** This represents the cardinality of the source entity records. For example, many means that multiple Weblog records are related to one WebAccount.
    - **Source lookup/link field:** This field represent the foreign key field in source entity. For example, WebLog has the accountId foreign key field.
    - **Target Entity:** The name of the entity that is used as a target in the relationship (for example, WebAccount).
    - **Target Cardinality:** This represents the cardinality of the target entity records. For example, one means that multiple Weblog records are related to one WebAccount.
    - **Target key field:** This field represent the key field of target entity. For example, WebAccount has the accountId key field.

**Note**: For now, only many-to-one and one-to-one type relationships are supported. Many-to-many type relationships can be created using two many-to-one relationships using a **link entity:** An entity that is used to connect the source entity and the target entity.

## Using the Relationships Screen to Delete Relationships
That can be easily done by:
1. Selecting the checkbox of the relationship/s you wish to delete:

   > [!div class="mx-imgBorder"] 
   > ![](media/select-relationship-to-delete.png "Select the relationship to delete")

2. Click **Delete** at the top of the relationship table:

   > [!div class="mx-imgBorder"] 
   > ![](media/delete-relationship.png "Delete relationship")

## Next Step
System and custom relationships are used in **Segment Editor Page** to navigate from the entity on one end of the relationship to the entity on the other end of the relationship as you define conditions to filter customers. Visit the **Segments** to learn more. Alternatively, you might want to define activities in your data - for that purpose visit the **Activites** section.


