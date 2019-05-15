---
title: "Virtual Agent Topic Checker"
description: "Virtual Agent Topic Checker"
keywords: ""
ms.date: 05/15/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Validate a topic and address errors with the Topic Checker

The Topic Checker is available in the conversation editor for any topic defined for your bot. It allows you to see the health of a topic and shows the errors and warnings that have failed validation. You can select the listed errors or warnings to go to the node or field that’s failed validation. As you fix the errors, they will disappear from the Topic Checker, either automatically or after saving the topic.

<<Topic checker Image>>

> [!IMPORTANT]
> You can save topics with errors. The errors will persist until they are addressed on the topic. Topics with errors may be deployed to production. However, unexpected behavior may result.

## Topic errors

The topic editor canvas validates topic and shows errors and warnings. Warnings will no prevent the bot from functioning and will be overlooked while processing. Errors should be addressed to avoid unexpected behavior or failure during the chat experience.
  
### Types of errors 

- Node: The entire node is erroneous and is highlighted red
- Field: The field is may be missing required data and is highlighted red
- Expression: The expression may be invalid and is highlighted red
- Variable deletion: A variable in a topic was deleted and is highlighted red wherever it was used. This causes the variable to become orphaned and must be either removed or replaced.
