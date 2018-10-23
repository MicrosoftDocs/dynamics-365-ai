---
title: "Market Insights scenarios for the marketing department | Microsoft Docs"
description: "Review marketing scenarios to get inspiration for how to efficiently leverage Market Insights in your organization."
keywords: "marketing, scenario, use case"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: 4ba36542-dce5-4944-a579-153decdc6ece
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Manage your brand and reputation on social media

[This topic is pre-release documentation and is subject to change.]

To successfully manage the reputation of your brand, it's essential to monitor the conversations about it on social media. Find out how the public perception of your brand is evolving and how you can actively engage with your customers.

This overview provides a step-by-step description of how you and your team can use [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] to monitor your brand reputation, review the performance of social media campaigns, engage with prospects, and find new leads for your sales team.

## Prerequisites

- [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] is [set up](settings-administration.md).

- [Search topics are configured](set-up-searches.md) and data acquisition is up and running. To listen to conversations about your brand, it's important that you create a search topic that gathers relevant posts.

- You have the required [user roles and permissions](user-roles.md) assigned in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].

## Brand reputation using AI

To find out how a brand is perceived on social media, after you [set up a search topic](set-up-searches.md) for it, [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] provides [sentiment analysis](analytics-sentiment.md) capabilities in the original language by using natural language processing and machine learning capabilities.

1. Get an overview of the posts that mention your brand on the [Overview page in Analytics](analytics-overview.md).

2. Go to **Analytics** > **Sentiment** to get insights into how people feel about your brand and find out who your brand advocates are.

3. See which topics are being discussed around your brand on the [Conversation page in Analytics](analytics-conversations.md).

## Get insights about demographics

For keyword searches, you'll get insights into the [age](analytics-overview.md#age) and [gender](analytics-overview.md#gender) of the audience that searches for similar terms on Bing. For example if you're planning a sports event, this information can be very helpful to prepare for the right number of facilities and changing rooms.  
Currently, these charts are only available in the United States. 

## Campaign performance

Campaigns on social media often revolve around a specific term, for example a hashtag. If you set up a search topic for this term, [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] helps you understand at a glance how your campaign is performing.

1. Get started analyzing the conversations about your campaign on the [Conversation page in Analytics](analytics-conversations.md).

2. [Create an activity map](activity-maps.md) to see newly found posts on a map with location data in real time.

3. Review the sentiment of posts that mention your brand on the [Sentiment page in Analytics](analytics-sentiment.md).

## Find leads for the sales team

Identify potential leads on social media and let your sales team know about them. [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] lets you create new leads in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] directly from a post within [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].

1. Use [intention analysis](tags.md#how-intention-analysis-works) to look for posts that express a purchase intent.

2. [Link these posts to Dynamics 365](create-dynamics-365-record-from-social-post.md) to create a new lead record.

3. Automate this workflow by using an [automation rule](automation-rules.md) for every post tagged with **Purchase Intention**.

## Share your content on social media

Have you launched or refreshed a product or service? Let your marketing team share it with the world. Publish posts and engage with your communities on social media with [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].

1. [Add social profiles](manage-social-profiles.md) and [share](manage-social-profiles.md#share-a-social-profile-with-other-users) them with your team.

2. [Publish](publish-react-posts.md) your news to social networks to spread the word about your products and services.

3. Work with [Office 365 groups](office-365-groups.md) to share social profiles or streams with a larger team.

## Customer stories

- [Port aims to proactively address issues using social media](https://customers.microsoft.com/story/port-aims-to-proactively-address-issues-with-microsoft)

- [Marston's delivers personalized service in real time with Dynamics 365](https://customers.microsoft.com/story/marstons-delivers-personalized-service-in-real-time-wi)

### See also

[Market Insights overview](overview.md)    
[Get started with Market Insights](get-started.md)    
[Manage connections in Market Insights](manage-connections.md)    
[Engage on social networks](engage-on-social-networks.md)
