---
title: "Use Microsoft Flow in your virtual agent"
description: "Learn how to use Microsoft Flow in your virtual agent."
keywords: ""
ms\.date: 1/7/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Use Microsoft Flow in your virtual agent

You can use flows created using Microsoft Flow in your virtual agent as long as the flows and virtual agent share the same CDS environment.

## To use flows in your virtual agent

1. If you do not already have a Microsoft Flow environment, log in to the Flow admin portal and create one. Enter [https://us.tip1.flow.microsoft.com/en-us/]( https://us.tip1.flow.microsoft.com/en-us/) in your browser to open the Flow portal.

2. Once you are logged in, verify that:

    - There is a Solution tab present, which indicates that you are on the updated Flow portal version.
    - You can access Settings in the top right corner of the screen.
    - There is an Admin Center option under Settings.

   > [!div class="mx-imgBorder"]
   > ![Flow portal](media/how-to-flow-1.PNG)

3. Choose **Admin Center**, which opens in a new tab. Then select the **New Environment** button in the upper right of the screen to create a new environment.

    Specify a unique name, set Region to *Preview (United States) (default)*, set Environment Type to *Trial*, and select the **Join Preview** box. 

   > [!div class="mx-imgBorder"]
   > ![Create environment](media/how-to-flow-2.PNG)

    Click **Create Environment** to save the environment and open the **Do you want to create a database?** screen.

4. Click **Create database** to display the **Create a database for this environment** screen.

   > [!div class="mx-imgBorder"]
   > ![Create database](media/how-to-flow-3.PNG)

5. Select your currency type (USD) and language (English), and then Click **Create Database**.

   > [!div class="mx-imgBorder"]
   > ![Create database environment](media/how-to-flow-4.PNG)

    **Note:**  Creating a database and environment can take several hours.

6. Once you have created your environment, return to the Flow portal and switch to the newly created environment to create your flows. Click on your User icon in the upper right corner and select your new environment from the dropdown list.

   > [!div class="mx-imgBorder"]
   > ![Open environment](media/how-to-flow-5.PNG)

    Make sure that the database was created correctly in your new environment by going to the Solutions page and verifying that Common Data Services Default Solution has been created for you.

   > [!div class="mx-imgBorder"]
   > ![Verify database](media/how-to-flow-6.PNG)

7. Create a flow in the Common Data Services Solution. Click **Common Data Services Solution**, select **+New**, and then select **Flow** from the dropdown list.

   > [!div class="mx-imgBorder"]
   > ![Create flow](media/how-to-flow-7.PNG)

    For example, you can create a simple flow that takes an email address as input parameter, sends an email message to that address, and returns a message that the email was successfully sent to a virtual agent as output.