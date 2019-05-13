---
title: "Virtual Agent Topic Checker"
description: "Virtual Agent Topic Checker"
keywords: ""
ms.date: 05/10/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Topic Checker and Error Validation
Topic checker allows you to see the health of your Topic.  It will show the errors and warnings that have failed validation.  You can select the listed errors or warnings to go to the node or field that’s failed validation.

## Errors
to understand what you will see in the Topic Checker you will need to understand the types of error messages and validation provided to the Bot Author.  
<<Node with error Image>>
### Types of errors: 
There are three different kinds of errors provided: 
1. Full Page
2. Banner messages
3. AUthoring canvas
The authoring canvas provides by errors and warnings.  Warnings will no prevent the bot from functioning and will be overlooked while processing.  Errors must be cleared up and will cause unexpected behaviors or critical failures during the chat experience.  
Errors and validations occur: 
1. Node - the whole node is in error and is highlighted red
2. Field - the field is may be missing required data and is highlighted red
3. Expresion - the expression may be invalid and is highlighted red
4. Variable deletion - in vairious scenarios, a variable within a topic may be deleted and is everywhere the variable was used is highlighted red. This causes the variable to become orphaned and must be either removed or replaced. 

## Topic Checker
The Topic Checker collects all the errors and warnings and allows you to click on an error or warning and the authoring canvas will center on that particular issue.  As you fix the errors, they will disappear from the Topic Checker, either automatically or when you click save.  Expect to see similar errors repeated in the topic checker as there may be many of similar type needing attention.
<<Topic checker Image>>
### Topics with errors
You may save topics with errors.  The errors will persist until they are cleared on the topic.  Topics with errors may be deployed to production, however unexpected behavior may result.
<<Save with errors Image>>  
