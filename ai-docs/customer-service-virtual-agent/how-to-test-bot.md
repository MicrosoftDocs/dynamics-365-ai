---
title: "Work with the Test Bot"
description: "Learn how to work with the AI for Customer Service Virtual Agent Test Bot."
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

# Work with the Test Bot

As you design your virtual agent in the Virtual Agent Designer, you can use the Test Bot to see how the virtual agent leads a customer through the virtual agent's conversation path. To help you find and fix unexpected behavior, you can enable tracing to take you through the conversation path step by step, and navigate to the corresponding node in the conversation editor.

## To test a topic in the Test Bot

1. At the **Type your message** prompt at the bottom of the Test Bot pane, enter a trigger phrase for the topic.

   > [!div class="mx-imgBorder"]
   > ![Trigger phrase](media/create-topic-20.png)

    The trigger phrase starts the topic's conversation, and the Test Bot displays the bot responses and user response choices you specified.

   > [!div class="mx-imgBorder"]
   > ![Start conversation](media/create-topic-21.png)

2. Continue the conversation path until you complete the conversation.

   > [!div class="mx-imgBorder"]
   > ![Complete conversation](media/create-topic-22.png)

3. To restart the conversation, select **Start over with latest content** at the top of the Test Bot pane.

   > [!div class="mx-imgBorder"]
   > ![Restart conversation](media/create-topic-23.png)

You can return to the conversation editor at any time to revise the topic's conversation path.

As you fine-tune your virtual agent, it can be useful to enable tracing to take you through the conversation path step by step.

## To trace through the topic's conversation path

1. In the upper-left corner of the Test Bot, select the **Conversation Tracing** toggle button to enable tracing.

   > [!div class="mx-imgBorder"]
   > ![Enable tracing](media/how-to-test-bot-1.png)

2. Follow the steps discussed earlier to [test your topic in the Test Bot](#to-test-a-topic-in-the-test-bot).

3. As you move through the conversation in the Test Bot, the conversation editor highlights the current place in the conversation path.

   > [!div class="mx-imgBorder"]
   > ![Test bot place](media/how-to-test-bot-2.png)

    The conversation editor displays highlighted nodes in green with check marks.

   > [!div class="mx-imgBorder"]
   > ![Conversation editor place](media/how-to-test-bot-3.png)

4. To navigate to an earlier place in the conversation path, select a bot or user response in the Test Bot.

   > [!div class="mx-imgBorder"]
   > ![Earlier place test bot](media/how-to-test-bot-4.png)

    The conversation editor highlights that node.

   > [!div class="mx-imgBorder"]
   > ![Earlier place conversation editor](media/how-to-test-bot-5.png)

If the conversation path in the Test Bot moves from one topic to another topic, the conversation editor refreshes and moves between topics to the appropriate highlighted nodes.
