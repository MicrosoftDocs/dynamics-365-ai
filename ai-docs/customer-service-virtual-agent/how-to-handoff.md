---
title: "Hand off a virtual agent conversation to a live agent"
description: "Learn how to use the Virtual Agent Designer to create a virtual agent conversation that hands off to a live agent."
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

# Hand off a virtual agent conversation to a live agent

A virtual agent can resolve many customer support issues, but there might be times when an issue requires a live agent. As you design the conversation path for your virtual agent's topics, you can include a handoff to a live agent by using the Escalate system topic.

## To add a handoff to a live agent

1. Select **Topics** in the navigation pane to open the Topics page.

   > [!div class="mx-imgBorder"]
   > ![Open Topics page](media/create-topic-1-1.png)

2. Hover over the Escalate system topic, and then select the **Edit** icon to open the topic in the conversation editor.

   > [!div class="mx-imgBorder"]
   > ![Edit Escalate topic](media/how-to-handoff-1.png)

3. In the **Bot Says** box, replace the *[link]* placeholder with a link to your engagement hub chat canvas.

   > [!div class="mx-imgBorder"]
   > ![Replace placeholder](media/how-to-handoff-2.png)

4. Select **Save** to save the topic.

   > [!div class="mx-imgBorder"]
   > ![Save topic](media/how-to-handoff-3.png)

5. Open the topic where you want to add the handoff in the conversation editor. Navigate to where you want to add the handoff, and then select **Escalate**.

   > [!div class="mx-imgBorder"]
   > ![Select Escalate](media/how-to-handoff-4.png)

    The Virtual Agent Designer adds an **Escalate** node to the conversation path.

   > [!div class="mx-imgBorder"]
   > ![Add Escalate node](media/how-to-handoff-5.png)

6. Select **Save** to save the topic.

   > [!div class="mx-imgBorder"]
   > ![Save topic](media/how-to-handoff-6.png)

7. Test your virtual agent in the Test Bot to see how the handoff works for customers.

   > [!div class="mx-imgBorder"]
   > ![Test handoff](media/how-to-handoff-7.png)
