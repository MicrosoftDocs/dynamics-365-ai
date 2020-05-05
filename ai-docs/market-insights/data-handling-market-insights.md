---
title: "Data handling R in Dynamics 365 Market Insights | Microsoft Docs"
description: "How Market Insights handles data, and how you can delete or export your data."
ms.date: 03/27/2020
ms.service: dynamics-365-ai
ms.topic: article
author: m-hartmann
ms.author: mhart
ms.custom: dyn365-ai-marketinsights
search.audienceType: 
  - admin
  - customizer
  - enduser
search.app: 
  - D365CE
  - D365SE
---

# Data handling for Dynamics 365 Market Insights

[!INCLUDE [market-insights-eos](../includes/market-insights-eos.md)]

(This topic is pre-release documentation and is subject to change.)

To run and improve the service for Market Insights Preview, we need to store some user data. This article is directed at users of the Market Insights Preview service. It outlines which data we gather, why we store it, and how you can request to export your data, update your name in the app, or delete your personal data.

Dynamics 365 Market Insights Preview includes capabilities to allow users to manage their personal data.

## Data storage in Market Insights alerts

The following data is stored:

- **Profile information** from the initial sign-up to sign you in again and access the app and your configuration
    - **Account information** (type of account) you use to sign in to recognize your profile when signing in again
    - **First and last name** to display your name in the app
    - **Email address** to send notification emails to the right recipient
- **List of elements (Universe)** that you selected and set properties for, to provide insights for topics you're interested in
- **Clicks** on news article links in the notification email to improve the relevance of insights sent to you
- **Read rate** of email messages for usage statistics
- **Feedback** you provide about the relevance of the notification email to improve the Market Insights service
- **Visits** to the Market Insights Preview website for usage statistics; includes the location (city level) from where the user calls the website

## Delete your data

Each user can [delete their user account](settings.md#delete-your-account) to remove their profile information in Market Insights, their universe, and all shared insights. Deleting the account will also stop all email notifications from Market Insights Preview.

> [!IMPORTANT]
> If you delete your account, all data will be removed and can't be restored. Even after signing in with the same profile again, your universe will be empty and your preferences will be reset to the default state.

## Request export of your data

To have your data exported, send us an [email](mailto:micustreqs@microsoft.com) and our team will follow up with you.

## Update your name in the app

To change your name in the app, update it on the profile you used to sign in. The app will sync your updated name from the profile directly. 
