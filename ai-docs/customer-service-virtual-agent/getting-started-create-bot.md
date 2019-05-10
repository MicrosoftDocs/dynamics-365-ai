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

To help get you started and tailor the bot to your specific needs, Virtual Agent lets you create a bot using built-in industry-specific templates. For example, Virtual Agent includes a template to help you create a bot for a retail business.

Each template comes with built-in content building blocks containing topics, trigger phrases, and pre-authored conversation paths that are tailored to a specific industry. For example, the Retail template includes a topic that lets you easily communicate store hours to customers.

These industry templates can also be useful as a model for building your own conversations for similar customer-support issues. For more information, see [Work with templates](how-to-templates.md).

## To create a bot

1. If you have not already created a PowerApps environment, create one. You must select an environment when you create your bot.

    For more information about creating a PowerApps environment, see [Creating a PowerApps environment](getting-started-new-environment.md).

2. Navigate to [https://va.ai.dynamics.com](https://va.ai.dynamics.com) in your browser to open the Virtual Agent environment and display the **Create a new bot** screen. Dynamics 365 Virtual Agent for Customer Service supports Chrome (preferred) and Edge browsers.

    If you have already created a bot, you can create a new bot by selecting the **New Bot** icon on the title bar. Then select **New bot**.

   > ![New bot icon](media/new-bot-icon.png)

3. Select the template you want to use, and specify a name and region for the bot.

    In the **Region where your bot is stored** drop-down, select the PowerApps environment you created. Then select **Create**.

    > [!NOTE]
    > Do not select the Default environment, which is not currently supported.

    Virtual Agent creates the bot and opens it in the browser.

   > ![Open bot](media/open-bot.png)

Once you have created your bot, you can add topics that represent the customer intents to be addressed by the bot and then deploy it to a web channel. As customers use the bot, you can view analytics information to help you improve it and the overall customer experience.

For more information about creating topics for your bot, see [Creating custom topics for your bot](getting-started-create-topics.md).

For more information about deploying your bot, see [Deploying your bot](getting-started-deploy.md).

For more information about using analytics information to help you improve your bot, see [Using analytics to improve your bot](getting-started-analytics.md).

For more information about working with Virtual Agent, see [Working with Virtual Agent](getting-started-bot-designer.md).

For information about removing your bot from the Virtual Agent environment, see [Deleting a bot](getting-started-delete-bot.md).
