---
title: "Preview: Relationships | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/01/2018
ms.reviewer: ""
ms.service: "crm-online"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# Preview: Relationships

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - This feature currently has limited availability.
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]  
> - [!INCLUDE[cc_preview_features_no_MS_support](../includes/cc-preview-features-no-ms-support.md)]  

In Dynamics 365 AI for Customer Insights, *Relationships* are also available for segmentation, insight-extraction and all other purposes. The *Relationships page* shown below includes five columns. We will explore these from left to right:
- **Relationship Name**: That is the name that you, as a user, assign to that relationship so it will be considered as an entity
- **Source Entity**: That is the name of the entity that is used as a source in that unidirectional/bidirectional relationship 
- **Source Cardinality**: Number that represents the number of nodes of the source entity. For example, if the number is 2 it means that two sources lead to one/more target entities in that relationship.
- **Target Entity**: That is the name of the entity that is used as a target in that relationship
- **Target Cardinality**: Number that represents the number of nodes of the target entity. For example, if the number is 1 it means that the source entity/entities lead to only one target entity.

- Lastly, the available actions on that page includes adding a new relationship or deleting a relationship as highlighted below

> [!div class="mx-imgBorder"] 
> ![](media/add-relationships.png "Add relationships")