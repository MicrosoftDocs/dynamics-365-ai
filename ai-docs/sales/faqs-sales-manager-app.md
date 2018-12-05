---
title: "Frequently asked questions for Dynamics 365 AI for sales | MicrosoftDocs"
description: "Frequently asked questions for Dynamics 365 AI for sales app"
keywords: "FAQs, Dynamics 365 AI for sales, AI for sales, Sales AI"
ms.date: 10/31/2018
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

# Frequently asked questions for sales manager capabilities

## Dynamics 365 AI for Sales app

**What languages are supported now?​**<br>
The application supports English (en-us) for tenants in the US region. We will support more languages in future releases

**When will you expand to support my region?**<br>
We plan to enhance our region availability by Spring 2019.

**Can I add my own reports?**<br>
No, currently we provide out-of-the-box visualizations and charts only. If you require more capabilities please leave us a suggestion at [Dynamics 365 AI for Sales communities](https://aka.ms/aisalescommunities) page.

**Are goals required to use the app?**<br>
No, however it is recommended to setup Revenue goals for each seller to get even better insights into the performance of your team. For more information please read [Create or edit a goal (Sales and Sales Hub)](/dynamics365/customer-engagement/sales-enterprise/create-edit-goal-sales).

**When will this product be Generally Available (GA)?**<br>
We are targeting Spring 2019 for GA.

**Can sellers (or non-managers) use this app?**<br>
The application is currently designed to bring the most value to sales managers. The application cannot provide much of value for sellers though they can use this application.

**Is an admin needed to enable the app for my organization?**<br>
No, up to 5 sales managers can use the application before the system administrator is required to log in.

## Call intelligence

**Which telephony system do you support?​**<br>
We support all telephony system. If you have call recordings, we process it at scale to generate insights​.

**What does the onboarding experience include?​** <br>
As part of the onboarding experience, you must provide the access key to the Azure blob location where you upload your call recording files for processing. You must adhere to standard metadata format (in JSON) of Call intelligence and upload that along with every call recording file. Apart from this, You must share keywords (also called Trackers) that you care about along with the competitive brands and products for Call intelligence to tracks these words across calls.

**Can I use this product for Customer service?​**<br>
Call intelligence is supporting Sales scenario for now. If you have call recordings for customer service, you can still use Call intelligence to gather and analyze Key KPIs customer service. Though few KPIs might be irrelevant for customer service.​

**What language is supported now?​**<br>
Call intelligence is supported for English (en-us) and US region only.​

**How is the sentiment model built?**<br>
Call intelligence transcribes the calls into text and generates sentiments from the words in the conversation. Call intelligence actively working on emotion model that leverages the vocal tones in the conversation for future releases.​

**I have mono-channel recording files. Can I still use Call intelligence?​**<br>
Yes, you can but the transcription accuracy will be poor as we don’t support mono-channel now. We are actively working to open the support for mono-channel in future releases.

**How long does it take to see the results?​**<br>
We don’t have a definitive time. Call intelligence takes several minutes to process and display the data on the screen depending on the audio size and format. 

**Can sellers see these insights?**<br>
No, sellers cannot see the insights. We will make the insights available for sellers in future releases​.

**Do you retain the call recordings?​**<br>
No, the call recordings will be deleted as soon as the audio file is processed​.