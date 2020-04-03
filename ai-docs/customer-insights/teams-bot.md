---
title: "Teams bot | Microsoft Docs"
description: "Look up unified customer profiles from Customer Insights in Microsoft Teams with the help of a bot."
ms.date: 04/03/2020
ms.reviewer: mhart
ms.service: dynamics-365-ai
ms.topic: "teams-bot"
author: stefanie-msft
ms.author: sthe
manager: shellyha
---

# Work with the Customer Insights Teams bot

Connect Dynamics 365 Customer Insights with Microsoft Teams to let a bot look up unified customer profiles in Teams channels.

## Prerequisites

To set up and configure the bot, the following prerequisites must be met:

- There's at least one [data source added](pm-data-sources.md).
- The [unification process](pm-configure-data.md) is complete.
- Fields are added to the [search and filter index](pm-manage-search.md).
- Customer Insights and Microsoft Teams are in the same organization.

## Set up and configure the bot

1. In Customer Insights, go to **Admin** > **Export Destinations**.
1. On the Microsoft Teams tile, select **Set up**.
1. You're redirected to the **Apps** area in Teams. Alternatively, open Teams and select **Apps** in the bottom left corner.
1. Search for **Dynamics 365 Customer Insights** and select the app.
1. Select **Add**.
1. After signing in to Customer Insights in Teams, you'll see a welcome message and can get started.

## Things you can do with the bot

The bot provides lookup capabilities for unified customer profiles.

- Enter **search** and append a name, email address, or any other field on the unified customer profile that is added to the search and filter index.

  The bot will present a card with up to 15 fields from the resulting customer profile. If there are multiple matches, you can select the profile to see from a list of results.

- If your organization maintains multiple Customer Insights instances in the same org, you can enter **switchinstance** to choose which instance you want to connect the bot to.

- Enter **help** to see a list of available commands for the bot.  
