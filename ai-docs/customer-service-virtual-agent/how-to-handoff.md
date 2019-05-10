---
title: "Hand off a bot conversation to a live agent"
description: "Learn how to use Virtual Agent to create a bot conversation that hands off to a live agent."
keywords: ""
ms.date: 05/10/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Hand off a bot conversation to a live agent

A bot can resolve many customer support issues, but there might be times when an issue requires a live agent. As you design the conversation path for your bot's topics, you can include a handoff to a live agent by using the Escalate system topic.

## To add a handoff to a live agent

1. Select **Topics** in the navigation pane to open the Topics page.

   > ![Open Topics page](media/open-topics.png)

2. Hover over the Escalate system topic, and then select the **Edit** icon to open the topic in the conversation editor.

   > ![Edit Escalate topic](media/open-escalate.png)

3. In the **Bot Says** box, replace the *[link]* placeholder with a link to your engagement hub chat canvas. Then select **Save** to save the topic.

   > ![Save topic](media/replace-placeholder.png)

4. Open the topic where you want to add the handoff in the conversation editor. Navigate to where you want to add the handoff, and then select **Escalate**.

   > ![Select Escalate](media/select-escalate.png)

    Virtual Agent adds an **Escalate** node to the conversation path.

   > ![Add Escalate node](media/add-escalate.png)

5. Select **Save** to save the topic, and then test your bot in the Test bot pane to see how the handoff works for customers.