---
title: "Working with the Virtual Agent Designer"
description: "Learn how to work with the Virtual Agent Designer."
keywords: ""
ms\.date: 12/5/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Working with the Virtual Agent Designer

The Virtual Agent Designer provides a variety of tools that make it easy to create a powerful custom virtual agent. You can add topics to your bot to help you design a conversation path to resolve customer support issues, and then deploy the bot to a support channel. You can also view analytics information to help you improve the bot and the overall customer experience.

The Virtual Agent Designer is composed of several pages designed for different tasks. You can navigate to the different pages by clicking in the navigation pane.

   > [!div class="mx-imgBorder"]
   > ![Navigation pane](media/bot-designer-1.PNG)

## Home page

   > [!div class="mx-imgBorder"]
   > ![Home page](media/create-bot-3.PNG)

The Home page provides a summary of the performance of your bot once it has been deployed, showing:

* The total number of support sessions that used the bot.
* The number and percent of resolved sessions.
* The number and percent of escalated sessions.
* The number and percent of sessions that were abandoned.
* The average customer satisfaction score of cases that use the bot.
* The hours saved as a result of using the bot.

## Analytics page

   > [!div class="mx-imgBorder"]
   > ![Analytics page](media/bot-designer-3.PNG)

The Analytics page provides a variety of dashboards and charts showing key performance indicators for your bot.

For more information about using the Analytics page, see [Using bot analytics to improve your bot](getting-started-analytics.md).

## Topics page

   > [!div class="mx-imgBorder"]
   > ![Topics page](media/bot-designer-4.PNG)

The Topics page is the central location for creating and managing bot topics, the customer intents that you use to design a conversation path. The Virtual Agent Designer includes several built-in system topics, as well as additional built-in topics specific to the template you use to create your bot.

You can revise the template topics and also create your own custom topics to design a conversation path that leads each customer to a resolution of the support issue. You can then test the bot in the Test Bot pane, and refine it as necessary.

For more information about using the Topics page to create topics, see [Creating topics for your bot](getting-started-create-topics.md).

## Deploy page

   > [!div class="mx-imgBorder"]
   > ![Deploy page](media/bot-designer-5.PNG)

The Deploy page is where you activate your completed bot to a support channel. This is where you can select the web channel for your bot, either the out-of-the-box test web page or your own custom web site.

As part of the deployment to the test web page, you can specify a custom welcome message and any suggested conversation starters to help customers get started using your bot.

   > [!div class="mx-imgBorder"]
   > ![Custom message](media/bot-designer-5-1.PNG)

If you choose to deploy your bot to your own custom web site, you will be able to copy and share the Virtual Agent code, which needs to be added to your custom web site.

For more information about using the Deploy page to deploy your bot, see [Deploying your bot](getting-started-deploy.md).

## Test Bot

Each page includes a Test Bot pane, where you can test your bot and view how the conversation with the bot works in practice.

You can test a bot topic by entering a trigger phrase for the topic at the **Type your message** prompt at the bottom of the test bot pane.

   > [!div class="mx-imgBorder"]
   > ![Trigger phrase](media/bot-designer-6.PNG)

    The trigger phrase starts the topic's conversation, and the Test Bot displays the bot responses and user response choices you specified when you created the topic on the Topics page.

   > [!div class="mx-imgBorder"]
   > ![Complete conversation](media/create-topic-22.png)