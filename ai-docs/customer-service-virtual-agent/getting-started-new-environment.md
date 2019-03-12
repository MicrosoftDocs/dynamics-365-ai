---
title: "Creating a PowerApps environment"
description: "Learn how to create a PowerApps environment for a Dynamics 365 Virtual Agent for Customer Service."
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

# Creating a PowerApps environment

When you create a virtual agent, you must select a PowerApps environment for the virtual agent. You can use an existing environment or create one.

If you encounter problems creating an environment, see [Known issues with creating a PowerApps environment](#known-issues-with-creating-a-powerapps-environment) later in this topic.

## To create a new PowerApps environment

1. Enter [https://admin.powerapps.com](https://admin.powerapps.com) in your browser to open the PowerApps Admin center.

2. Select **New environment** to open the New environment screen.

    Specify a unique name for the environment, *United States* as the region, and *Trial* as the environment type. Then select **Create environment**.

   > ![Create environment](media/create-environment.png)

    PowerApps creates the environment and displays a prompt asking if you want to create a database.

3. Select **Create database** to display the **Create a database for this environment** screen.

   > ![Create database](media/create-database.png)

4. Select your currency type and language, and then select **Create database**.

   > ![Create database](media/create-database2.png)

> [!NOTE]
> Creating a database and environment can take some time.

## Known issues with creating a PowerApps environment

Dynamics 365 Virtual Agent for Customer Service uses the Common Data Service (CDS) as the primary storage technology for virtual agent content. When you create your virtual agent PowerApps environment, you may encounter issues with:

* Having sufficient permissions for the CDS environment.
* Creation of a virtual agent timing out after a long delay.

### Having sufficient permissions for the CDS environment

You may not be able to create a virtual agent if you do not have sufficient permissions for the CDS environment. You must have read/write access to the environment. You may encounter this issue if:

* You do not have read/write access to any CDS environment. In this case, Virtual Agent for Customer Service displays the following error:

    "You do not have access to any environment. Please get access from an administrator."

* You do not have sufficient privileges for the selected CDS environment. In this case, Virtual Agent for Customer Service displays the following error:

    "An unexpected server error occurred. Please retry creating your bot."

To resolve this issue, follow the steps in [To create a new PowerApps environment](#to-create-a-new-powerapps-environment) to create a new environment. Use that environment to create your virtual agent.

### Creation of a virtual agent timing out after a long delay

Creating a virtual agent for the first time may take a long time even if you have sufficient permissions to the CDS environment. Creation of the Virtual Agent may eventually succeed. If so, Virtual Agent for Customer Service displays the Virtual Agent Designer home page. However, it may time out, generating the following error:

"An unexpected server error occurred. Please retry creating your Virtual Agent."

If you receive this error, refresh your browser. In most cases, the virtual agent creation succeeds despite the error. If it did not succeed, retry the Virtual Agent creation.