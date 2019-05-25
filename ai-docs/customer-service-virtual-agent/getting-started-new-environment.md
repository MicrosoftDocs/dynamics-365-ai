---
title: "Creating a PowerApps environment"
description: "Learn how to create a PowerApps environment for Dynamics 365 Virtual Agent for Customer Service."
ms.date: 05/23/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Creating a PowerApps environment

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

When you create a bot, you must select a PowerApps environment for the bot. You can use an existing environment or create one.

## To create a new PowerApps environment

Watch the [step-by-step video](https://go.microsoft.com/fwlink/?linkid=2079331), or follow these steps:

1. Go to [https://admin.powerapps.com](https://admin.powerapps.com) and sign in using your work or school account.

2. Select **New environment** to open the **New environment** dialog box.

    Specify a unique name for the environment, select **United States** as the region, and select the environment type. Then select **Create environment**.

    ![Create environment](media/create-environment.png)

    PowerApps creates the environment and displays a prompt asking if you want to create a database.

3. Select **Create database** to display the **Create a database for this environment** screen.

   ![Create database](media/create-database.png)

4. Select your currency and language, and then select **Create database**.

   ![Create database](media/create-database2.png)

    > [!NOTE]
    > Creating a database and environment and making it available in Dynamics 365 Virtual Agent for Customer Service can take a couple of minutes.

5. You are now ready to use the environment when [creating a new bot](getting-started-create-bot.md).

