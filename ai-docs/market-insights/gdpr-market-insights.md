---
title: "Data handling and GDPR in Dynamics 365 Market Insights | Microsoft Docs"
description: "How Market Insights handles data, and how you can file a DSR."
ms.date: 09/25/2019
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

# Data handling and GDPR for Dynamics 365 Market Insights

(This topic is pre-release documentation and is subject to change.)

To run and improve the service for Market Insights Preview, we need to store some user data. This article is directed at users of the Market Insights Preview service. It outlines which data we gather, why we store it, and how you can request to export your data, update your name in the app, or delete your personal data.

The GDPR gives people (known in the GDPR as data subjects) specific rights to their personal data, including the ability to: obtain copies of personal data, request corrections or deletions, restrict processing of personal data, or to receive personal data in an electronic format so it can be moved to another controller. The controller is the organization that collects and makes use of the personal data.

A formal request by a data subject to a controller to take an action on their personal data is called a Data Subject Request (DSR).

Dynamics 365 Market Insights Preview includes capabilities to fulfill its obligations to data subjects when they raise requests to manage their personal data.

## Data storage in Market Insights alerts

The following data is stored:

- **Profile information** from the initial sign-up to sign you in again and access the app and your configuration
    - **Account information** (type of account) you use to sign in to recognize your profile when signing in again
    - **First and last name** to display your name in the app
    - **Email address** to send notification emails to the right recipient
- **List of elements (Universe)** that you selected and set properties for, to provide insights for topics you're interested in
- **List of alerts** that were created for you to present you articles you may be interested in
- **Clicks** on news article links in the notification email to improve the relevance of insights sent to you
- **Read rate** of email messages for usage statistics
- **Feedback** you provide about the relevance of the notification email to improve the Market Insights service
- **Visits** to the Market Insights Preview website for usage statistics

## Delete your data

Each user can [delete their user account](settings.md#delete-your-account) to remove their profile information in Market Insights, their Universe, and all shared insights. Deleting the account will also stop all email notifications from Market Insights Preview.

> [!IMPORTANT]
> - If you request deletion of your data, all data will be removed and can't be restored. Even after signing in with the same profile again, your universe will be empty and your preferences will be reset to the default state.

## Request export of your data

To have your data exported, send us an [email](mailto:micustreqs@microsoft.com) and our team will follow up with you.

## Update your name in the app

To change your name in the app, update it on the profile you used to sign in. The app will sync your updated name from the profile directly. If this doesn't work, send us an [email](mailto:micustreqs@microsoft.com) and request the change.
