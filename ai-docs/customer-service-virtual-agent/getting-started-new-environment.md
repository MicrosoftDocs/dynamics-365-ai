---
title: "Creating a PowerApps environment"
description: "Learn how to create a PowerApps environment for Dynamics 365 Virtual Agent for Customer Service."
keywords: ""
ms.date: 05/20/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Creating a PowerApps environment


[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

When you create a bot, you must select a PowerApps environment for the bot. You can use an existing environment or create one.

If you encounter problems creating an environment, see [Known issues with creating a PowerApps environment](#known-issues-with-creating-a-powerapps-environment) later in this topic.

## To create a new PowerApps environment



> [!NOTE]
> Watch this step-by-step video: [Create a new PowerApps environment](https://go.microsoft.com/fwlink/?linkid=2079331)


1. Enter [https://admin.powerapps.com](https://admin.powerapps.com) in your browser to open the PowerApps Admin center.

2. Select **New environment** to open the New environment screen.

    Specify a unique name for the environment, *United States* as the region, and *Trial* as the environment type. Then select **Create environment**.

    ![Create environment](media/create-environment.png)

    PowerApps creates the environment and displays a prompt asking if you want to create a database.

3. Select **Create database** to display the **Create a database for this environment** screen.

   ![Create database](media/create-database.png)

4. Select your currency type and language, and then select **Create database**.

   ![Create database](media/create-database2.png)

> [!NOTE]
> Creating a database and environment can take some time.

## Known issues with creating a PowerApps environment

When you create your bot's PowerApps environment, you may encounter issues with:

* Having read/write access to any environment.
* Having sufficient privelege for the selected environment.
* Creation of a bot timing out after a long delay.


### Having read/write access to any environment

In this case, you will see this error: “You do not have permissions to any environments. Please get access from an administrator.”

To resolve this issue, follow the steps in [To create a new PowerApps environment](#to-create-a-new-powerapps-environment) to create a new environment. Use that environment to create your bot.


### Having sufficient privelege for the selected environment

Ideally the region (environment) dropdown UI should only contain environments a user has read/write access to; however, the dropdown is not currently constrained that way, we are working to fix this. If the user selects an environment that she has insufficient access to, she will get the following error: “An unexpected server error occurred. Please retry creating your bot.”

To resolve this issue, follow the steps in [To create a new PowerApps environment](#to-create-a-new-powerapps-environment) to create a new environment. Use that environment to create your bot.


### Creation of a bot timing out after a long delay

When creating the first bot in an environment, there is a known issue where the bot creation takes a long time and either:

1.	Eventually succeeds and lands the user on the Virtual Agent home screen OR
2.	Errors out as in case above

Workaround: If 2. occurred, and you are sure you had sufficient environment privileges  (i.e., you created the environment as guided above), then proceed as follows:
    Refresh your browser
    After the refresh, in most cases, you will find that the bot creation succeeded despite the error; else retry the bot creation again.
