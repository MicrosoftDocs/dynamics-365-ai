---
title: "Relationships | Microsoft Docs"
description: Connect entities to create segments and measures from multiple data sources in Dynamics 365 Customer Insights.
ms.date: 04/01/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Relationships

Relationships help you connect entities and generate a graph of your data. Relationships are used when entities share a common identifier (foreign key) that can be referenced from one entity to another. Connected entities enable you to define segments and measures based on multiple data sources.

> [!div class="mx-imgBorder"]
> ![Relationships tile](media/configure-data-relationships-tile.png "Relationships tile")

There are two types of relationships:

- **System relationships**: These are created by the system automatically and cannot be edited.
- **Custom relationships**: These are created by the user during configuration and can be edited.

During the match and merge processes, system relationships are created behind the scenes based on intelligent matching. These relationships help relate the Customer Profile records with other corresponding entities' records. The following diagram exemplifies the creation of three system relationships when the customer entity is matched with additional entities to produce the final Customer Profile entity.

> [!div class="mx-imgBorder"]
> ![Relationship creation](media/relationships-entities-merge.png "Relationship creation")

- ***CustomerToContact* relationship** was created between the Customer entity and the Contact entity. The Customer entity gets the key field **Contact_contactId** to relate to the Contact entity key field **contactId**.
- ***CustomerToAccount* relationship** was created between the Customer entity and the Account entity. The Customer entity gets the key field **Account_accountId** to relate to the Account entity key field **accountId**.
- ***CustomerToWebAccount* relationship** was created between the Customer entity and the WebAccount entity. The Customer entity gets the key field **WebAccount_webaccountId** to relate to the WebAccount entity key field **webaccountId**.

## The Relationships page

In addition, you can use the **Relationships** page to define custom relationships as shown here.

> [!div class="mx-imgBorder"]
> ![Customer relationships](media/relationships-custom.png "Custom relationships")

Each relationship has two key parts:

- **Source entity**: Represents the entity that holds the foreign key.
- **Target entity**: Represents the entity that the source entity’s foreign key points to.

To create a relationship, first select **Add relationship**.

> [!div class="mx-imgBorder"]
> ![Add relationships](media/add-relationships.png "Add relationships")

Next, provide the following information in the **Relationship** pane.

> [!div class="mx-imgBorder"]
> ![Enter relationship details](media/relationships-add.png "Enter relationship details")

- **Relationship name**: You can provide a meaningful name that reflects the purpose of the relationship (for example, **AccountWebLogs**).
- **Description**: Friendly description of the relationship.
- **Source entity**: The name of the entity that is used as a source in the relationship (for example, WebLog).
- **Cardinality**: This represents the cardinality of the source entity records. For example, “many” means that multiple Weblog records are related to one WebAccount.  
- **Source lookup/link field**: This represents the foreign key field in the source entity. For example, WebLog has the **accountId** foreign key field.
- **Target entity**: The name of the entity that is used as a target in the relationship (for example, WebAccount).
- **Target cardinality**: This represents the cardinality of the target entity records. For example, “one” means that multiple Weblog records are related to one WebAccount.
- **Target key field**: This field represents the key field of target entity. For example, WebAccount has the **accountId** key field.

> [!NOTE]
> For now, only many-to-one and one-to-one relationships are supported. Many-to-many relationships can be created using two many-to-one relationships and a link entity—an entity that is used to connect the source entity and the target entity.

## How to delete a relationship

To delete a relationship:

1. Select check boxes for the relationships you want to delete.

   > [!div class="mx-imgBorder"]
   > ![Select the relationship to delete](media/select-relationship-to-delete.png "Select the relationship to delete")

2. Select **Delete** at the top of the **Relationships** table.

   > [!div class="mx-imgBorder"]
   > ![Delete relationship](media/delete-relationship.png "Delete relationship")

## Next step

System and custom relationships are used in the **Segment Editor page** to create segments based on multiple data sources that are no longer siloed. Visit the **Segments** section to learn more. Alternatively, you might want to define activities in your data. Visit the **Activities** section.
