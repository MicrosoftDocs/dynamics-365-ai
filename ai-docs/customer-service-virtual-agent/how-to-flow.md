---
title: "Use Microsoft Flow with your virtual agent"
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

# Use Microsoft Flow with your virtual agent

You can use flows created using Microsoft Flow in your virtual agent as long as the flows and virtual agent share the same CDS environment.

## To create a Microsoft Flow environment

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

Once you have created your environment, return to the Flow portal and switch to the newly created environment to create your flows.

## To create a flow

1. Click on your User icon in the upper right corner and select your new environment from the dropdown list.

   > [!div class="mx-imgBorder"]
   > ![Open environment](media/how-to-flow-5.PNG)

    Make sure that the database was created correctly in your new environment by going to the Solutions page and verifying that Common Data Services Default Solution has been created for you.

   > [!div class="mx-imgBorder"]
   > ![Verify database](media/how-to-flow-6.PNG)

2. Create a flow in the Common Data Services Solution. Click **Common Data Services Solution**, select **+New**, and then select **Flow** from the dropdown list.

   > [!div class="mx-imgBorder"]
   > ![Create flow](media/how-to-flow-7.PNG)

    For example, you can create a simple flow that takes an email address as input parameter, sends an email message to that address, and returns a message that the email was successfully sent to a virtual agent as output.

3. Select a trigger for your flow. A Virtual Agent Designer virtual agent can only invoke flows that have HTTP request interfaces. Enter *HTTP* in the Search box, and select **When HTTP request is received** to create a flow with an HTTP request trigger.

   > [!div class="mx-imgBorder"]
   > ![Select trigger](media/how-to-flow-8.PNG)

4. Add the following JSON code in the **Request Body JSON Schema** box. The code specifies that the flow expects an email address to receive one string input parameter.

    ``` JSON
        {  
        "type": "object",  
            "properties": {  
                "to": {  
                    "type": "string"  
                }  
            }  
        }
    ```

   > [!div class="mx-imgBorder"]
   > ![Add JSON code](media/how-to-flow-9.PNG)

5. Specify that an email message should be sent to the email address specified in the input. Enter *Outlook* in the Search box and select **Send an email** to create a connection to Microsoft Outlook using your Outlook credentials to send the message.

   > [!div class="mx-imgBorder"]
   > ![Send email](media/how-to-flow-10.PNG)

6. Specify an email address for the message, and fill in the Subject and Body fields.

    You can specify a Flow input variable (“to”) as the recipient address using Dynamic Content. Click **See more** to see all dynamic variables.

   > [!div class="mx-imgBorder"]
   > ![Create message](media/how-to-flow-11.PNG)

7. If you specify the “to” variable as the recipient address, click **New step** to return a message to the flow.

   > [!div class="mx-imgBorder"]
   > ![Return message](media/how-to-flow-12.PNG)

8. Use an HTTP Response to return a variable to the virtual agent. Enter *Response* in the search box and select the **Response** action in the search results list.

   > [!div class="mx-imgBorder"]
   > ![HTTP response](media/how-to-flow-12.PNG)

9. Specify the following information for the Response action, and then save your flow.

   > [!div class="mx-imgBorder"]
   > ![Response action](media/how-to-flow-13.PNG)
