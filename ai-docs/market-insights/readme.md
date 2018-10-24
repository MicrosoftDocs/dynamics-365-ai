---
title: "Market Insights 2018 Update 1.8 Readme"
description: "Important and late-breaking information about Dynamics 365 AI for Market Insights"
keywords: "readme, known issues, information"
ms.date: 10/31/2018
ms.service: dynamics-365-ai
ms.topic: article
ms.assetid: d7cce391-9d1d-4284-b040-a29b55fa87c0
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

# [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] Readme

[This topic is pre-release documentation and is subject to change.]

This document provides important, late-breaking information about [!INCLUDE[Dynamics 365 AI for Market Insights](../includes/pn-market-insights-long.md)].

Do you have an idea how to further improve the service or app? Go to the [Ideas forum for Market Insights](https://experience.dynamics.com/ideas/list/?forum=0a0bebf4-8bef-e511-80ba-00155d03a726) and let us know. For questions and feedback in general, please go to the [Community forum](https://community.dynamics.com/crm/f/752).

## Integration scenarios - known issues

### Microsoft Dynamics 365 domains must be added to Allowed Domains to enable integration

For the integration between Microsoft Dynamics 365 and [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)], your Dynamics 365 [domains must be added as allowed domains in Market Insights](connect-other-domains.md).
This will ensure that only the Dynamics 365 domains you own can make requests to your data.

If you are a [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] administrator, you can do this by going to **Settings** \> **Allowed Domains**. Add only your owned Dynamics 365 domains as allowed domains to enable communication with [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].

## Display of content - known issues

### Blog content delivered in some cases in JSON format

For some blogs coming through WordPress, the format of the text is not delivered in the usual format, but instead in JSON format, which diminishes the readability of the content considerably.

### YouTube videos in tweets are not always rendered in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)]

In the case where a video is shared directly from YouTube to Twitter, the video is not rendered in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)]. Instead the link to the video is displayed in the respective tweet.

### A News post might not contain an original URL

In addition to online news, the [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] **News** source includes publications that are not publicly available on the web. In that case, no link to the original source is available for the post.

### No author details for authors of Twitter retweets and Facebook shares

Even though there is an author detail icon next to the name of an author whose post has been retweeted or shared, there is no author detail available for such an author. The UI will show the message: “No author details are available”.

## Search setup - known issues

### Changing search topic category not reflected in the UI   

When the category on an existing search topic is changed, the search topic still shows the previously selected category. Although the changes are saved, you need to refresh the browser to see the change reflected correctly. 

### Facebook Acquisition Notification in Analytics does not always disappear

In some cases, the notification in Analytics that tells [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] users that they do not have a valid token for Facebook Pages acquisition is wrongly displayed.

If you see this message, we recommend you go to Social Profiles and check whether your acquisition tokens are valid. If they are valid, you can ignore the notification.

### Some Disqus posts are not acquired due to a missing URL in the post

In some cases, Disqus posts are missing a URL. This can happen if posts are created through an API or through private channels. [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] cannot acquire messages that are missing a URL.

### Private messages and public messages from Facebook Pages and Twitter not always acquired

In some cases, private messages and public messages from Facebook Pages and Twitter are not acquired in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)]. This can happen when a message was written in a non-supported language of [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] or if the language was not detected at all.

## General known issues

### Facebook video URL can expire

Due to changes from Facebook, some videos are not playing anymore in [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)]. This is due to an expiration of the video URL. There is no workaround available to change the expiration. You can view the video directly from the Facebook post.

### Analytics does not display social profiles added in the same session until you refresh your browser

If you add a social profile and then go straight to **Analytics**, the social profile is not immediately displayed as a source to publish in publish actions.

To resolve this, manually refresh your browser after adding a social profile.

### Sharing with all users for social profiles and streams has high-visibility consequences

Owners of social profiles and streams have the option to choose **Shared** and share content and publish actions with all users. These are the implications of taking this action:

-   For a social profile: Every user with the Interaction role "Manager" or "Responder" will be able to use the social profile in the publish actions within [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].

-   For a stream: Every user will see this stream on their Social Center page. Because there is no way to hide a stream, we recommend that you use this option with restraint.

### Notifications that trigger multiple actions might overlap

When you perform multiple actions within a short time frame, notification messages might overlap. Although notifications disappear automatically, we recommend that you close them manually so that you can see each notification and take action as needed.

### Quota notification in Search Setup can be hidden and is hard to show again

When you go to the **Search Setup** area, you might see the quota warning notification that your solution might be or is already above quota. You can hide this notification by selecting the **Close** (X) button in the upper right corner. Once it’s closed, you can only get it back by refreshing your browser’s session with [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)].

### [!INCLUDE[Market Insights](../includes/pn-market-insights-short.md)] stops responding after you select the Include button

In Microsoft Edge or Internet Explorer, if you select too many authors and then select **Include**, the Authors widget in Full view mode might stop responding. The workaround is to refresh your browser, select fewer authors, and select **Include** again.