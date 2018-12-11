---
title: "Work with the Test Bot"
description: "Learn how to work with the AI for Customer Service Virtual Agent Test Bot."
keywords: ""
ms\.date: 12/11/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Work with the Test Bot

As you design your AI for Customer Service Virtual Agent bot, you can use the Test Bot to see how the virtual agent leads a customer through the bot's conversation path. To help you find and fix unexpected behavior, you can enable tracing to take you through the conversation path step by step, and quickly navigate to the corresponding node in the conversation editor.

## To test a topic in the Test Bot

1. Open the topic and click **Edit conversation** to open the conversation editor.

   > [!div class="mx-imgBorder"]
   > ![Edit conversation](media/create-topic-8-1.png)

    You can also select the topic in the topics list and click the edit icon.

   > [!div class="mx-imgBorder"]
   > ![Edit conversation](media/create-topic-8.png)

2. To make the topic available to the Test Bot, click **Push to Test** in the upper right corner of the Bot Designer.

   > [!div class="mx-imgBorder"]
   > ![Push to test](media/create-topic-19.png)

3. At the **Type your message** prompt at the bottom of the Test Bot pane, enter a trigger phrase for the topic.

   > [!div class="mx-imgBorder"]
   > ![Trigger phrase](media/create-topic-20.png)

    The trigger phrase starts the topic's conversation, and the Test Bot displays the bot responses and user response choices you specified.

   > [!div class="mx-imgBorder"]
   > ![Start conversation](media/create-topic-21.png)

4. Continue the conversation path until you complete the conversation.

   > [!div class="mx-imgBorder"]
   > ![Complete conversation](media/create-topic-22.png)

5. To restart the conversation, click **Restart conversation** at the top of the chat bot pane.

   > [!div class="mx-imgBorder"]
   > ![Restart conversation](media/create-topic-23.png)

You can return to the conversation editor at any time to revise the topic's dialog, and continue to fine-tune the bot until you are ready to deploy it.