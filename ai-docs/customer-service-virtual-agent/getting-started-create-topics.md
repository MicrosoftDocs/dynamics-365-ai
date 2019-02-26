---
title: "Creating topics for your virtual agent"
description: "Learn how to use the Virtual Agent Designer to create topics for your virtual agent."
keywords: ""
ms.date: 2/26/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Creating topics for your virtual agent

A topic defines a conversation path with the virtual agent for a specific customer intent. You specify a trigger phrase that prompts the virtual agent to start the conversation. Then create a conversation path in the Virtual Agent Designer's conversation editor to lead customers to a resolution of their support issue.

You can see how the conversation path works in practice by testing it in the Test Virtual Agent and continue to fine-tune the topic until you are ready to deploy it.

## To create your own topic

1. Select **Topics** in the navigation pane to open the Topics page.

   > ![Open Topics page](media/open-topics.png)

    The Topics page displays a list of your virtual agent's current topics, including a variety of built-in topics.

    The Virtual Agent Designer includes industry-specific topics, depending on the template you used to create your virtual agent. For example, the Retail template includes topics for finding out a store's hours, looking up the balance of a gift card, or paying a bill.

   > ![Built-in topics](media/template-topics.png)

    The Virtual Agent Designer also includes several system topics that help you address common situations--a customer greeting, escalation to a live agent, the end of the conversation, a confirmed success, or a confirmed failure.

2. On the Topics page, select **New topic**.

   > ![New topic](media/create-new-topic.png)

3. Specify a name, description, and one or more trigger phrases for the topic.

    A trigger phrase is a phrase that a customer enters in the chat window to start a conversation with the virtual agent. Once the conversation is started, the conversation follows the path you define. You can specify more than one trigger phrase for a topic.

    Then select **Save topic** to add the topic to the topics list.

   > ![Save topic](media/save-topic.png)

## To design the topic's conversation path

1. Select **Edit** to open the conversation editor.

   > ![Edit conversation](media/edit-conversation.png)

    The Virtual Agent Designer opens the topic in the conversation editor and displays the topic's trigger phrases. The conversation editor is where you define the conversation path between a customer and the virtual agent.

   > ![Open conversation](media/open-conversation.png)

2. Enter the virtual agent's response to the trigger phrase in the **Bot says** box.

   > ![Add bot response](media/bot-response.png)

3. To specify an additional response by the virtual agent, select **Bot says**.

   > ![Additional bot response](media/add-response.png)

    Then enter the additional response in the **Bot says** box.

   > ![Additional response text](media/response-text.png)

4. To specify a response by the customer, select **User says**.

    You can provide several options for the user’s response. The options display as clickable buttons.

   > ![Add user response](media/user-says.png)

    Enter a response in the **User responses** box.

   > ![Add user response text](media/user-response.png)

    To give the customer a choice between different responses, select **Add user response**.

   > ![Additional user response](media/second-response.png)

    Then specify the additional response in the **User responses** box.

   > ![Additional user response text](media/second-response-text.png)

    The conversation editor creates separate paths in the conversation, depending on the customer's response. The conversation path leads the customer to the appropriate resolution for each user response.

5. Add additional bot and user responses to complete the conversation path.

   > ![Complete conversation](media/complete-conversation.png)

6. To add a customer satisfaction survey at the end of a response that resolves the customer issue, select **End with survey**.

   > ![End with survey](media/end-with-survey.png)

   Then select **Save** to save the conversation path.

As you design your topic's conversation path, you can use the Test Virtual Agent to see how the virtual agent leads the customer through a conversation with the virtual agent.

## To test the topic in the Test Virtual Agent

1. At the **Type your message** prompt at the bottom of the Test Virtual Agent pane, enter a trigger phrase for the topic.

   > ![Trigger phrase](media/enter-trigger.png)

    The trigger phrase starts the topic's conversation. The Test Virtual Agent displays the bot and user responses that you specified in the conversation editor.

   > ![Start conversation](media/start-conversation.png)

2. Continue the conversation path until you complete the conversation.

   > ![Complete conversation](media/complete-test.png)

3. To restart the conversation, select **Start over with latest content** at the top of the Test Virtual Agent pane.

   > ![Restart conversation](media/restart-conversation.png)

You can return to the conversation editor at any time to revise the topic's conversation path and continue to fine-tune the virtual agent until you are ready to deploy it. For information on deploying your virtual agent, see [Deploying your virtual agent](getting-started-deploy.md).

For more information on using the Test Virtual Agent, see [Work with the Test Virtual Agent](how-to-test-bot.md).
