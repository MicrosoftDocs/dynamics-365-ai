---
title: "Frequently asked questions for Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Frequently asked questions for Dynamics 365 Sales Insights app"
keywords: "FAQs, Dynamics 365 Sales Insights, AI for sales, Sales AI, Sales Insights"
ms.date: 07/31/2019
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 673c693b-9265-4641-bb31-a72b8a97bb3a
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Frequently asked questions for Sales Insights application

**What languages are supported now?​**<br>
The application supports the following model languages:

- Brazilian Portuguese (pt-BR)
- Chinese (simplified) (zh-CN)
- English - United States (en-US)
- English - Great Britain (en-GB)
- French - France (fr-FR)
- German - Germany (de-DE)
- Italian - Italy (it-IT)
- Japanese - Japan (ja-JP)
- Spanish - Spain (es-ES)
- Spanish - Mexico (es-MX)

The application supports the following machine learning model languages for contextual insights capabilities:

- English

**When will you expand to support my region?**<br>
The application is supported in the following regions:

- Canada (CAN)
- Europe, the Middle East, and Africa (EMEA)
- Great Britain (GBR)
- India (IND) 
- Japan (JPN)
- North American (NAM)
- Oceania (OCE)

**How long does it take for data updates to reflect in the app?**<br>
The data is refreshed periodically and could take up to 12 hours to reflect. We continue to make improvements to reduce this delay.

**Can sellers (or non-managers) use this app?**<br>
Yes, the application is also available for sellers and can view their conversational insights.

**Is an admin needed to enable the app for my organization?**<br>
Yes. Administrator must configure the application for you to use. If administrator did not configure the application, you can explore the application with the demo data that is provided.

**Which telephony system do you support?​**<br>
The application is independent of telephony systems. If you have stereo call recordings (two-channel stereo), we process them at scale to generate insights​.

**What does the onboarding experience include?​** <br>
As part of the onboarding experience, you must provide the access key to the Azure blob location where you upload your call recording files for processing. You must adhere to standard metadata format (in JSON) of conversation intelligence and upload that along with every call recording file. Apart from this, you must share trackers that you care about along with the competitive brands and products for conversation intelligence to track these words across calls.

**How is the sentiment model built?**<br>
Conversation intelligence transcribes the calls into text and generates sentiment from the text in the conversation.

**I have mono-channel recording files. Can I still use conversation intelligence?​**<br>
No, we DO NOT process mono-channel call recording files. We only support stereo-type call recording files.

**How long does it take to see the results?​**<br>
Conversation intelligence takes a few minutes to process and display the data on the dashboard, depending on the size of the call recording files and format. You must have at least 10 call recording files to process and display the data.

**Do you retain the call recordings?​**<br>
No. The call recordings are deleted as soon as the audio file is processed​.

### See also

- [View home page](dynamics365-sales-insights-app-home-page.md)

- [View team information](conversation-intelligence-team-overview.md)

- [View seller information](conversation-intelligence-seller-details.md)