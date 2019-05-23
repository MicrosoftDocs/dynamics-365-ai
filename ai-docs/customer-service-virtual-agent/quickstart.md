---
title: "Quickstart: Create and deploy a customer service bot"
description: "Learn how to quickly create a customer service bot using Virtual Agent."
ms.date: 05/16/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Quickstart: Create and deploy a customer service bot

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

Microsoft Dynamics 365 Virtual Agent for Customer Service empowers customer teams to quickly and easily create powerful bots using a guided, no-code graphical experience – all without the need for data scientists or developers. 

This guide will take you through the end-to-end experience of creating a bot for the first time, adding custom topics to your bot, testing content changes in real-time, deploying your bot to a test page, and analyzing the performance of your bot after it’s been deployed. You can also [view this video](http://go.microsoft.com/fwlink/?linkid=2062988) that works through the end-to-end process. 

## Creating your first bot

1.	Navigate to [http://aka.ms/virtual-agent](http://aka.ms/virtual-agent) in your browser to begin. Supported browsers include Edge, Chrome, and Firefox. On the website, select **Try Preview**, then sign-in with your work email address. Please note that personal Microsoft accounts aren't supported currently.
    ![Sign up page](media/sign-up-screen.png)

2. Next, you’ll choose a name for your bot. This can be something generic to your company or specific to the scenario you would like to tailor your bot towards.
By default, your bot will be created in the default PowerApps environment that was created for you when signing up. For most users, this is sufficient. However, if you want to specify a custom PowerApps environment for your virtual agent, you can do so by expanding the “More options” menu and selecting a different environment.
   > [!NOTE] 
   > Preview is currently only supported in the US, with data stored in US data centers.  If your company is domiciled outside of the US, you will need to create a custom environment with Region set to “United States” before you can create your virtual agent.  For more information on how to create a custom PowerApps environment, see Creating a PowerApps environment.

   ![Name the new bot](media/create-new-bot-screen.png)

3.	Once you select **Create**, the next process can take up to 15 minutes for the first bot to be created within a new environment.  

4. After a few minutes, you’ll land on the Home page and have an opportunity to play around with the bot in “read-only” mode.  While you can't save any edits during this time, you can explore the overall user interface, look at the topics, experiment with the pre-loaded User Topics and System Topics, and interact with your bot using the Test Canvas.  During this time, you can also watch product videos to learn how to complete tasks such as creating a branching dialogue tree using variables and expressions, or creating a Flow and embedding Flows within your dialogue tree.
    
   ![Read-only mode](media/create-bot-banner-blue.png)

5. When the bot creation process completes (up to 15 minutes for the first bot creation), you’ll see the banner change – you now have full functionality in the bot and can modify any User or System Topic, test out your content changes, or deploy your bot.

   ![Green banner after creating bot](media/create-bot-banner-green.png)

## Creating a custom Topic

1.	Now that you have full functionality within your bot, you can create your own custom topic – or in other words, a dialogue tree specifying how your bot responds to a user’s question. Here's a [video about creating a topic](http://go.microsoft.com/fwlink/?linkid=2063539).

2.	Start by selecting **Topics** in the left-hand navigation panel, then select **+ New topic** at the top of the page.
    ![New topic](media/create-new-topic.png)

3. You can now name your topic and include some trigger phrases for this topic. Trigger phrases are examples of the type of user questions or utterances that help teach the bot when to respond with this dialogue. As an example, let’s create a Topic called “Personal Hello World” and add “hello world” as a trigger phrase.  Select **Save topic** and then select **Edit** to proceed.

4. After saving your topic, you will land in the conversation editor – this is the graphical dialogue tree editor that allows you to define the bot responses and overall conversation flow.
Start by entering “Hello! I’ll create a personalized greeting for you.” into the first Bot Says node. Then, add another Bot Says node by selecting it in the menu below the first Bot Says node.

5. In the second Bot Says node, enter “Where do you live?” and select **User Says** from the menu below the second Bot Says node. Select **+ Add user response**. 

6. For the two “User Says” responses, enter “Seattle” and “Bellevue” in the User Responses node. Now, enter “Hello Seattle!” in the Seattle branch on the left, and “Hello Bellevue!” in the Bellevue branch on the right. Select **Save** in the upper right-hand corner.

You now have a very simple, branching dialogue tree – congratulations!  Of course, you can begin to create more complex versions of this tree by incorporating variables, expressions, and Microsoft Flow.

## Testing your content in real-time

1.	Now that you have some content authored into a dialogue tree, it’s time to test this out in real-time and see if it’s working as you expected. For this, you’ll use the Test bot panel. Begin by selecting the **Start over with latest content** button near the top of this panel.
 
    If the Test bot is not showing on your screen, select the **Test your bot** button in the lower left-hand corner of your screen.

2.	Now that the latest content has been refreshed in the test bot, you can try out your newly authored dialogue tree by typing into the test bot window. Turn on **Tracing** at the top – this will enable you to follow along with the bot as it executes your dialogue. You’ll start to see parts of your dialogue tree highlighted as the bot gets to that portion of the dialog.

3.	Type "hello world" in the chat window and send the message to the bot. You’ll see the top portion of your dialogue tree highlighted in green, and you’ll see “Seattle” and “Bellevue” presented as user options in the test bot window.
The bot is now waiting for you to respond and has provided suggestions on how to respond. These suggestion buttons reflect what you authored within your dialogue tree in the “User Responses” node.  In the test bot, you can either click on these suggestion buttons to continue, or you can type your response in the chat window.  
	 

4.	You can continue the dialog by selecting the Seattle branch. You’ll see the dialogue stop once you’ve reached the bottom of this branch.  If you author more content, the dialogue will continue – but since we’ve only created a very simple and small dialogue tree, we can reach the end of the content very quickly.

    This test experience empowers you to quickly create and test a conversation to ensure that the conversation will flow as anticipated. If the dialogue does not reflect your intention, you can change the dialogue, save it, push the latest content into the test bot, and try it out again. None of this changes the deployed version of the bot, so feel free to play around with your content until you are happy with it.
 

## Deploying your bot

1.	Once you are fine with the content authored in your bot, you can deploy your bot to a website. Start by selecting the **Deploy** tab in the left-hand navigation pane.

    You’ll now see two options – one to deploy to a Demo website, and one to deploy to a Custom website. The custom website provides a snippet of code to send to your website administrator. This embeds the bot canvas into the website of your choosing so that your end users can interact with your bot from your web channel.

    At this point, it’s premature to deploy your bot to your website, so let’s start with the demo website instead. Select **Demo website**.
 

2.	Enter a welcome message and conversation starters that will be displayed on your demo website.
For now, enter “This is a demonstration of my first bot that I built by myself, without writing a line of code!” in the Welcome message, and “Hello world” in the Conversation starters. Select the **Publish** button.
 
3.	A new window opens in your browser. If this doesn’t happen automatically, check if a pop-up blocker has been activated and allow the window to be opened. This is a webpage that demonstrates what your bot looks like to an end-user who comes to your webpage. The bot canvas is in the lower right-hand corner, and you can interact with it by either typing into the window or by click on the “Hello world” conversation starter you added previously.
 

4.	You'll find a link added to the Deploy page. This link can be copied and shared with others in your organization and is a great way for others to experience the bot that you have created. This URL is also the same as the one shown in the test webpage.

    > [!NOTE]
    > Anyone with this link can interact with your bot using the test webpage shown above, so please do not share sensitive information in this bot. Your visitors will interact with your bot as an “end-user” but will not be able to see the conversation editor.


## Analyzing the performance of your bot

1.	Once your bot has completed interactions with users, the statistics are available via the **Analytics** tab in the left-hand navigation panel. Here, you can find key performance indicators (KPIs) showing the volume of sessions your bot has handled, how effectively your bot was able to engage end-users and resolve issues, escalation rates to human agents, and abandonment rates during conversations.  You will also find CSAT information at the KPI level as well as in the **Customer Satisfaction** tab.

    Note: There is up to a 1-hour delay between when the conversations occur and when the statistics for those conversations appear in the Analytics views.  Also, all interactions with the bot will be logged in analytics, including interactions from your demo website, custom website, or test bot.

2.	You can also view detailed session history and transcripts by selecting “Sessions” from the Analytics tab.  This enables you to download a CSV file with the full session transcript.  This can be a helpful way for you to tune the performance of your bot and change the content in your Topics to improve your bot’s efficiency.

You’ve now created a bot, created your own custom topic, tested it out, deployed it to a demo website, and learned how to analyze your bot’s performance.  Congratulations!  Your bot has many capabilities beyond this, so please try it out and play with the advanced features.