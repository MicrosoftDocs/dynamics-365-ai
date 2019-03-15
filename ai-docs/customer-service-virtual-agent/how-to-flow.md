---
title: "Add actions to your virtual agent using Microsoft Flow"
description: "Learn how to add actions to your virtual agent using Microsoft Flow."
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

# Add actions to your virtual agent using Microsoft Flow

You can enable you virtual agent to perform an action by invoking a Microsoft Flow. Use a flow that shares the same Common Data Service (CDS) environment as the virtual agent. First, create a Microsoft PowerApps environment and then create your flow. Once you have created the flow, you can create a virtual agent that uses an action to invoke the flow.

## To create a Microsoft PowerApps environment

1. If you have not already created a PowerApps environment, create one. You must select an environment when you create your virtual agent.

    For more information about creating a PowerApps environment, see [Creating a PowerApps environment](getting-started-new-environment.md).

2. If you do not already have a Microsoft Flow environment, log in to the Flow admin portal by entering [https://flow.microsoft.com]( https://flow.microsoft.com) in your browser. Click on the icon for your account in the upper right corner of the screen, and then select your PowerApps environment from the list.

3. Verify that the PowerApps environment database was created correctly. Select **Solutions** in the navigation pane to display the **Solutions** page, and then verify that the Solutions list includes **Common Data Services Default Solution**.

   > ![Verify database](media/verify-database.png)
   > [!NOTE]
   > Since creating a new environment can take some time, the new solution might not immediately appear in the list. Log out and check again in 30 to 60 minutes.

   Once you have created your environment, return to the Flow portal and switch to the newly created environment to create your flow.

## To create a flow

1. Select **Common Data Services Default Solution** to open the solution.

2. On the **Common Data Services Default Solution** page, select **+New**, and then select **Flow** from the list.

   > ![New flow](media/new-flow.png)

    You can create a variety of flows for your solution. For example, you could create a simple flow that takes an email address as an input parameter, sends an email message to that address, and returns a message that the email was successfully sent to a virtual agent as output.

3. Select a trigger for your flow. A Virtual Agent Designer virtual agent can only invoke flows that have HTTP request interfaces. Enter **HTTP** in the Search box, and select **When a HTTP request is received** to create a flow with an HTTP request trigger.

   > ![Select trigger](media/select-trigger.png)

4. Add the following JSON code in the **Request Body JSON Schema** box. The code specifies that the flow expects an email address to receive one string input parameter. Then select **New Step**.

    ``` JSON
    {  
        "type": "object",  
        "properties": {  
            "to": {  
                "type": "string"  
            }  
        }  
    }
    ```

   > ![Add JSON code](media/add-json-code.png)

5. Specify that an email message should be sent to the email address specified in the input. Enter **Outlook** in the Search box and select **Send an email** to create a connection to Microsoft Outlook. Follow the directions to specify your Outlook credentials and grant approval to access your account.

   > ![Send email](media/send-email.png)

    Microsoft Flow displays the **Send an email** window.

6. To use dynamic content as the recipient address, place your cursor in the **To** field to display the **Dynamic content** tab, and then select **See more**.

   > ![See more](media/see-more.png)

    To use the Flow input variable **to** as the recipient address, select **to**.

   > ![Create message](media/select-to.png)

7. Add text to the Subject and Body fields of the message, and then select **New step**.

   > ![Return message](media/return-message.png)

8. Use an HTTP Response to return a variable to the virtual agent. In the **Choose an action** window, enter **Response** in the search box, and then select the **Response** action.

   > ![HTTP response](media/http-response.png)

9. Specify the following information for the Response action, and then select **Show advanced options** to display the **Response Body JSON Schema** field.

   > ![Show advanced](media/show-advanced.png)

    Add the following JSON code to the **Response Body JSON Schema** field, and then select **Save**.

    ``` JSON
    {  
        "type": "object",  
        "properties": {  
            "message": {  
                "type": "string"  
            }  
        }  
    }
    ```

   > ![Response action](media/response-action.png)

## To create a virtual agent that invokes a flow

1. Navigate to [https://va.ai.dynamics.com](https://va.ai.dynamics.com) in your browser to open the Virtual Agent Designer environment, and then create a new virtual agent in the same environment as your flow. To create a new virtual agent, select the **New Bot** icon on the title bar. Then select **New bot**.

   > ![New bot icon](media/new-bot-icon.png)

    For more information about creating a virtual agent, see [Creating a virtual agent](getting-started-create-bot.md).

2. On the **Create a new bot** screen, specify a template, a unique name for your virtual agent, and the environment where your flow was created. Then select **Create**.

   > ![Specify environment](media/specify-environment.png)

3. Once you have created your virtual agent, create a topic that uses the flow. Select **Topics** in the navigation pane to open the **Topics** page, and then select **New topic**.

   > ![New topic](media/create-new-topic.png)

    For more information about creating a topic, see [Creating topics for your virtual agent](getting-started-create-topics.md).

4. Specify a name, description, and trigger phrases for the topic. A trigger phrase is a phrase that a customer enters in the chat window to start a conversation with the virtual agent. You can include punctuation in a trigger phrase, but it is best to use short phrases rather than long sentences.

    For example, for a *Daily Deals* topic, you could specify the following trigger phrases:

    - daily deals
    - deal of the day
    - current deals
    - today’s deals
    - current offers
    - today’s specials
    - current specials
    - special offers
    - today’s coupons
    - current coupons
    - today’s offers

    Then select **Save topic** to save the topic.

   > ![Save flow topic](media/save-flow-topic.png)

5. Once you have created the topic, you can create a conversation path that uses your flow. Select **Edit** to open the conversation editor.

   > ![Open flow conversation](media/open-flow-conversation.png)

    In the conversation editor, enter a virtual agent response in the **Bot Says** node, and then select **User says** to display the **User Responses** node.

   > ![Create conversation](media/create-conversation.png)

    In the user responses node, select **Add Variable** to display the **Properties** pane, where you can create a variable to save a customer's email address.

   > ![Add variable](media/add-variable.png)

    In the Properties pane, select **Create variable** to display the **Create new variable** window.

   > [!div class="mx-imgBorder"]
   > ![Create new variable](media/create-new-variable.png)

    For more information on creating variables, see [Work with variables](how-to-variables.md).

6. Specify a variable name and type. For example, you could create a text variable named **User_Email**.  Select **Done** to save the variable.

   > ![Save variable](media/create-flow-variable.png)

    The Virtual Agent Designer adds the variable to the **User Responses** node and creates an **Expression** node. You can delete this node if you do not want to do any validation.

   > ![Delete expression](media/delete-expression.png)

7. Select **Bot says** to add another node with text confirming that the email will be sent.

   > ![Confirmation node](media/confirmation-node.png)

    To display the specified email address in the user's conversation with the virtual agent, place your cursor in the **Bot Says** node to display the popup menu. Then select the variable you created from the variable drop-down list.

   > ![Select variable](media/select-variable.png)

8. To send a message to the specified email address in the user's conversation with the virtual agent, select **Action** to display the list of available actions, and then select the flow action you created.

    > ![Select action](media/select-action.png)
    > [!NOTE]
    > The flows and virtual agent must be created in the same environment. Otherwise, the flow action does not appear in the list of available actions.

    The Virtual Agent Designer creates an **Action** node indicating that the action has one required input and one output. Select the variable you created from the drop-down list to pass it as input.

   > ![Create action](media/create-action.png)

9. Add another **Bot Says** node to display the message from the flow to the customer. Place your cursor in the node to display the popup menu, and then select the **message** variable from the variable drop-down list.

   > ![Display flow message](media/display-flow-message.png)

10. Select **End with survey** to end your conversation with a survey, and then select **Save** to save the topic.

   > ![Flow topic end](media/flow-topic-end.png)

## To test the flow

1. In the Test Virtual Agent, select **Start over with latest conversation**. Then specify a trigger phrase for the topic that contains the flow.

2. Enter your email address at the prompt.

   > ![Test flow](media/test-flow.png)

    After you specify the email address, the flow sends an email message and returns the message to the virtual agent.

   > ![Successful flow](media/successful-flow.png)

    The Virtual Agent Designer stores the message in the **(x) message** variable and displays it to the customer.

   > ![Email message](media/email-message.png)