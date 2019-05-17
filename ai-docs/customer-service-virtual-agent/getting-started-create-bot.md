---
title: "Creating a bot"
description: "Learn how to use the Dynamics 365 Virtual Agent for Customer Service to create a bot."
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

# Creating a bot

You can use Virtual Agent to create a powerful custom bot. Virtual Agent makes it easy to create bots that address common support issues. You can design a conversation path that leads each customer to a resolution.

To help get you started and tailor the bot to your specific needs, Virtual Agent lets you create a bot using built-in content building blocks containing topics, trigger phrases, and pre-authored conversation paths. These built-in topics can also be useful as a model for building your own conversations for similar customer-support issues. For more information, see [Work with built-in topics](how-to-templates.md).

## To create a bot

1. If you have not already created a PowerApps environment, create one. You must select an environment when you create your bot.

    For more information about creating a PowerApps environment, see [Creating a PowerApps environment](getting-started-new-environment.md).

2. First bot creation: Navigate to [https://va.ai.dynamics.com](https://va.ai.dynamics.com) in your browser to open the Virtual Agent environment. Dynamics 365 Virtual Agent for Customer Service supports Chrome (preferred) and Edge browsers.

    If you are visiting for the first time, you will be taken through a wizard-like experience to sign-up and create your first bot. You will be going through the following steps:
    
    - Sign-up / create an account
    - Obtain the license – this will happen once per user (for public preview access)

    <<<<<<<<<< INSERT PICTURE OF NEW USER SCREEN >>>>>>>>>

    In the “Create a new Bot” dialog, give your bot a name and press **Create** 
  
    <<<<<<<<<< insert pic here of the new create bot dialog >>>>>>>>>
  
    Since this is your first bot, it might take a few minutes for everything to be setup. During this time, you can checkout some features of the virtual agent. You can chat with the test bot and follow along by tracing your conversation in the authoring canvas.
  
   Here are some of the things you will be able to do while your bot is getting created.
      a. Chat with a test bot
      b. View Topics
      c.	Edit topics (note that you cannot save them while your bot is getting created).
      d.	Trace your conversation in the authoring canvas.
      e.	Watch videos

   Once the bot is created you will see a message confirming that your bot is ready. At this point, you will have all functionality of the virtual agent available to you. However, while your first bot is getting created, the below features will be temporarily disabled:
      a. Saving changes – cannot save topics, cannot 'Start over with latest content’ in the test bot
      b.	Analytics, Deploy, and Settings are disabled.

  <<<<<<<<<<< insert pic here of the read-only bot experience UX screenshot >>>>>>>>>>>>

3. If you have already created a bot, you can create a new bot by selecting the **Bot** icon on the title bar, then selecting **New bot**. The rest of the experience is similar as above.

<<<<<<<<<<<<<<<<<<<<<<< insert pic here >>>>>>>>>>>>>>>>>>>>


4. In the 'Create a new bot' dialog when you create a bot, you could choose to expand the **More options** section and choose an environment for the bot. 

Once you have created your bot, you can add topics that represent the customer intents to be addressed by the bot and then deploy it to a web channel. As customers use the bot, you can view analytics information to help you improve it and the overall customer experience.

For more information about creating topics for your bot, see [Creating custom topics for your bot](getting-started-create-topics.md).

For more information about deploying your bot, see [Deploying your bot](getting-started-deploy.md).

For more information about using analytics information to help you improve your bot, see [Using analytics to improve your bot](getting-started-analytics.md).

For more information about working with Virtual Agent, see [Working with Virtual Agent](getting-started-bot-designer.md).

For information about removing your bot from the Virtual Agent environment, see [Deleting a bot](getting-started-delete-bot.md).
