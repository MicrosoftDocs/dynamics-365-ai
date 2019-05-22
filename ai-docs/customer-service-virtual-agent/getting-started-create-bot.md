---
title: "Creating a bot"
description: "Learn how to use the Dynamics 365 Virtual Agent for Customer Service to create a bot."
ms.date: 05/20/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Creating a bot

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

You can use Virtual Agent to create a powerful custom bot. Virtual Agent makes it easy to create bots that address common support issues. You can design a conversation path that leads each customer to a resolution.

To help get you started and tailor the bot to your specific needs, Virtual Agent lets you create a bot using built-in content building blocks containing topics, trigger phrases, and pre-authored conversation paths. These built-in topics can also be useful as a model for building your own conversations for similar customer-support issues. For more information, see [Work with built-in topics](how-to-templates.md).

## To create the first bot

If you encounter an issue while creating your bot, see [Known issues](#known-issues) below.

### Creating a bot - US based users

Watch the [step-by-step video](http://go.microsoft.com/fwlink/?linkid=2062988) or follow the steps below.

1. Navigate to [aka.ms/virtual-agent](http://aka.ms/virtual-agent) and select "Sign up". Sign up and if you are signing up for the first time, obtain a license and agree to the terms and conditions

2. In the **Create a new bot** dialog, give your bot a name and select **Create**. 

  > [!NOTE]
  > If you are based outside of US, you might have to create a new PowerApps environment located in the US. See [Creating a PowerApps environment](getting-started-new-environment.md) for more information on creating a new environment. Once you created a new environment located in the US, select **More options** and choose the correct environment. 
  
   ![Create a new bot](media/create-new-bot.PNG)
    
   > [!NOTE]
   > If this is your first bot, it might take a few minutes for everything to be set up. 
   >
   > Here are some things you can do to use this time and explore some features of Virtual Agent.
   > - [Chat with a test bot](how-to-test-bot.md#work-with-the-test-bot-pane)
   > - [Trace your conversation in the authoring canvas](how-to-test-bot.md#to-trace-through-the-topics-conversation-path)
   > - [View and edit topics](getting-started-bot-designer.md#topics-page) (but not save them)
   > - [Watch product videos](virtual-agent-videos.md)
   >
   > When everything is set up, you'll see a message confirming that your bot is ready. At this point, you will have all functionality available to you. 
   
3. You are now ready to [Create cutom topics for your bot](getting-started-create-topics.md)!

## Creating additional bots

If you have already created a bot, you can create a new bot by selecting the **Bot** icon on the title bar, then selecting **New bot**.

   ![New bot icon in title bar](media/new-bot-icon.png)

## Known issues with creating a bot

When you are creating your bot, you may encounter the following issues

### No read/write access to any environment

In this case, you will see this error: “You do not have permissions to any environments. Please get access from an administrator.”

To resolve this issue, follow the steps in [To create a new PowerApps environment](getting-started-new-environment.md) to create a new environment. Use that environment to create your bot.


### Insufficient permissions for the selected environment

If the user selects an environment that she has insufficient access to, she will get the following error: “An unexpected server error occurred. Please retry creating your bot.”

To resolve this issue, follow the steps in [To create a new PowerApps environment](getting-started-new-environment.md) to create a new environment. Use that environment to create your bot.
