---
title: "Create a PowerApps environment"
description: "Learn how to create a PowerApps environment for Dynamics 365 Virtual Agent for Customer Service."
ms.date: 06/19/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Create a PowerApps environment

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

When you create a bot, you must select a PowerApps environment for the bot. You can use an existing environment or create one.

<iframe width="560" height="315" src="https://www.youtube.com/embed/YL14y3jQbBE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## To create a new PowerApps environment

1. Go to [https://admin.powerapps.com](https://admin.powerapps.com) and sign in using your work or school account.

2. Select **New environment** to open the **New environment** dialog box.

    Specify a unique name for the environment, select **United States** as the region, and the environment type. Then select **Create environment**.

    > [!NOTE]
    > The environment needs to be created with the region set to **United States**, otherwise you won't be able to use it when creating a bot.
    > Trial environments expire after 30 days. You'll lose all bots created in the trial environment when it expires.

   ![Create environment](media/create-environment-2.png)

   PowerApps creates the environment and displays a prompt asking if you want to create a database.

3. Select **Create database** to display the **Create a database for this environment** screen.

   ![Create database](media/create-database.png)

4. Select your currency, language, and clear the checkbox for **Include sample apps and data** and then select **Create database**.

   > [!NOTE]
   > Clearing "Include sample apps and data" will speed up the process of environment creation.

   ![Create database](media/create-database-2-1.png)


5. You will know that the environment is ready when you see an its ID in parenthesis after the environment name. It might take up to 5 minutes before you are ready to use the environment when [creating a new bot](getting-started-create-bot.md).

    ![Environment is ready when string id is appended](media/environment-ready.png)




## Trial Environments


If you have created your own environment and selected Trial as the environment type, you will receive emails shortly before its expiration. Also, in the Virtual Agent Designer, you will see a message if you have bots created in a Trial environment that is going to expire in 14 days or less. The message will indicate the name of the environment that is going to expire, the days remaining to expiration, and the names of the bots affected. This pertains only to Trial environments that you have created yourself or been granted access to.

Trial environments expire after 30 days. When the environment expires, all the bots in the environment will be deleted and the data associated with it, the flows, and resources you have been using will be lost. The message indicates that you need to action before the environment expires.

While using the Trial environment, if you created bots you want to retain longer than 30 days, convert the Trial environment to a Production environment. To convert to a Production environment, these criteria must be met: • A suitable PowerApps plan. A plan that enables you to create Production environments. • Available Production quota. There are a fixed number of Production environments you can create with your plan. Follow the steps here to convert a trial environment to production.
