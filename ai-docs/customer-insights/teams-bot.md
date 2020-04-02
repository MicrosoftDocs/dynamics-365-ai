---
title: "Teams bot | Microsoft Docs"
description: "Get a consolidated view on you unified customer profiles in Dynamics 365 Customer Insights."
ms.date: 02/04/2020
ms.reviewer: sthe
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---
# Connect Microsoft Teams with Customer Insights 
You can now connect Dynamics 365 Customer Insights with Microsoft Teams, so that you and your employees can consume unified customer profiles with the help of a bot in Microsoft Teams. 
## Prerequisites
In order to configure Dynamics 365 Customer Insights in Microsoft Teams, make sure 
* you’ve created at least one data source within the **Data Sources** page 
* you’ve completed the M3 process.[link] 
* You’ve configured fields to be indexed for search. [link]
* You have access to both Customer Insights and to Microsoft Teams on the same tenant. 

## How to configure the bot
1.	In Dynamics 365 Customer Insights, navigate to **Export Destinations** and select **Set up** on the Microsoft Teams tile
2.	You get redirected to the **Apps**  on Microsoft Teams. Alternatively open Microsoft Teams and navigate to **Apps** in the bottom left corner. 
3.	Search for “Dynamics 365 Customer Insights (Preview)” app 
4.	Hit **Add** after you’ve found the “Dynamics 365 Customer Insights (Preview)” app
5.	The Customer insights bot welcomes you and you can get started (in case you are using the bot for the first time, you need to login first)
## What can you do with the bot?
The “Dynamics 365 Customer Insights bot allows you to look up unified customer profiles. To achieve this, simply type **search**, followed by a name, email address or other field on the unified customer profile that is being indexed for search. 
The bot will present a result or in case of multiple hits, a result list of matching customer profiles where you can select the one you were looking for. The bot will then present a card with up to 15 fields on the customer profile. 

If you happen to have multiple Dynamics 365 Customer Insights instances on the same tenant, you can apply the **switchinstance** command in the Microsoft Teams bot to choose which instance you want to connect to. 

Type **help** any time to see a list of available commands for the bot.  
