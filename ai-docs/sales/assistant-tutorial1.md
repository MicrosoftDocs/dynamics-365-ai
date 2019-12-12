---
title: "Tutorial on how to create a custom insight card for Assistant for Dynamics 365 Sales Insights | MicrosoftDocs"
ms.date: 12/05/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
---

# Tutorial 1: Hello world

## Objective

To create an insight card that displays "Hello world" every morning on your dashboard.

## Step 1: Create a trigger to start the flow

Set a trigger that runs every morning at 8 AM.

On the **Assistant Studio** page, select **+ Create a new insight card**, and then select **+ Create from blank**.

In the search box, enter **Recurrence**. In the search results, under **Triggers**, select **Recurrence**. You'll see the following trigger.

> [!div class="mx-imgBorder"]
> ![Search for the recurrence schedule option](media/assistant-tutorial-1-recurrence-search.png "Search for the recurrence schedule option")

Open the recurrence schedule trigger. Enter **Interval** as **1**, and select **Frequency** as **Day**. This ensures that the trigger will run once a day. Set **At these hours** to **8**, to run the trigger every morning at 8 AM.

> [!div class="mx-imgBorder"]
> ![Configure the recurrence schedule](media/assistant-tutorial-1-recurrence-settings.png "Configure the recurrence schedule")

## Step 2: Add an action to the flow

In the **Search connectors and actions** box, enter **Sales insights** or **Assistant**, and then select the **Dynamics 365 Sales Insights** connector. Under **Actions**, select **Create card for assistant**.

> [!div class="mx-imgBorder"]
> ![Search for the Sales Insights connector](media/assistant-tutorial-1-search-sales-insights-connector.png "Search for the Sales Insights connector")

If you haven't made a connection by using the Dynamics 365 Sales Insights connector, use your Dynamics 365 account to sign in.

> [!div class="mx-imgBorder"]
> ![Sign in to Sales Insights](media/assistant-tutorial-1-sales-insights-signin.png "Sign in to Sales Insights")

When you sign in, you'll see the following screen, where you can define the fields required to create a card.

> [!div class="mx-imgBorder"]
> ![Sales Insights card settings](media/assistant-tutorial-1-sales-insights-card-settings.png "Sales Insights card settings")

| Parameter | Description |
|-----------|-------------|
| **Environment** | The Dynamics 365 organization in which we're creating the card. You can choose your organization from the list. |
| **Card name** | The name of the card, which is displayed at the top of the card. This should be a simple string, with no special characters or dynamic content. |
| **Card header** | The title of the card, which appears just below the card name. |
| **Card text** | The text that's displayed in the body of the card. |
| **Button type** | The type of action to be performed when the button on the card is selected. It can be either **Open URL** or **Open Entity**. In this tutorial, we're leaving this at the default value of **Open URL**. |
| **Button URL/record ID** | Because the button type selected above is **Open URL**, we'll enter a URL to be opened. If the button type were **Open Entity**, we'd enter the record ID of the entity to be opened. |

## Step 3: Enter the information for the insight card

Enter the following information on the **Create card for assistant** screen. The other fields are optional and can be left blank for the purpose of this tutorial.

> [!div class="mx-imgBorder"]
> ![Enter the Sales Insights card settings](media/assistant-tutorial-1-sales-insights-card-information.png "Enter the Sales Insights card settings")

| Parameter | Value |
|-----------|-------|
| **Environment** | assistantstudio (or the name of your org)|
| **Card name** | Sample |
| **Card header** | Hello world |
| **Card text** | This is my sample flow card for **formatDateTime(utcNow(), 'D')**<br>(This expression gets the current date in the format **DayOfWeek, Month Day, Year**.)  |
| **Button type** | Open URL |
| **Button URL/record ID** | https://www.bing.com |

## Step 4: Save the flow

Select **Save** on the **Create card for assistant** screen.

<a name="test-the-flow"></a>
## Step 5: Test the flow

Testing ensures that the insight card has been configured properly. To test, select **Test** in the upper-right corner and follow the instructions.

> [!div class="mx-imgBorder"]
> ![Test your Sales Insights card](media/assistant-tutorial-1-sales-insights-test-options.png "Test your Sales Insights card")

Now, every morning at 8 AM you'll see a card on your Dynamics 365 dashboard that says "Hello world." The following image shows what the insight card will look like.

> [!div class="mx-imgBorder"]
> ![Sample Sales Insights card](media/assistant-tutorial-1-sample-insights-card.png "Sample Sales Insights card")

You can also see the card type on the **Assistant Studio** home page.

> [!div class="mx-imgBorder"]
> ![List of Sales Insights cards](media/assistant-tutorial-1-list-insights-cards.png "List of Sales Insights cards")

### See also

[Tutorial 2: Sample insight for each user in your org](assistant-tutorial2.md)