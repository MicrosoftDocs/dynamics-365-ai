---
title: "Work with variables"
description: "Learn how to work with Dynamics 365 Customer Service Virtual Agent variables."
keywords: ""
ms.date: 1/14/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Work with variables

Variables let you save responses from your customers in a conversation with a virtual agent so that you can reuse them later in the conversation. For example, you can save a customer's name in a variable called *UserName*. The virtual agent can then address the customer by name as the conversation continues.

You can use variables to create logical expressions that dynamically route the customer down different conversation paths.

Virtual Agent Designer supports four types of variables:

* String -- A string of text that the customer enters.
* Age -- A positive number within the range of standard age.
* Currency -- A numeric currency value.
* Number -- A single positive or negative integer.

## To create a variable

1. In the Virtual Agent Designer conversation editor, select the ellipses in the upper-right corner of the **User responses** node where you want to add the variable.

   > [!div class="mx-imgBorder"]
   > ![Click ellipses](media/how-to-variables-1.png)

2. Select **Properties** to open the Properties pane.

   > [!div class="mx-imgBorder"]
   > ![Open properties pane](media/how-to-variables-2.png)

3. Select **Name variable** to open the **Create variable** window.

   > [!div class="mx-imgBorder"]
   > ![Create variable](media/how-to-variables-3.png)

4. Specify a name and type for the variable, and then select **Save**.

   > [!div class="mx-imgBorder"]
   > ![Save variable](media/how-to-variables-4.png)

The Virtual Agent Designer adds the variable to a customer's response and uses expressions to dynamically route the conversation path, letting you tailor the virtual agent's response.

   > [!div class="mx-imgBorder"]
   > ![Save variable](media/how-to-variables-5.png)
