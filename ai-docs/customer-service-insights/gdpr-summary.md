---
title: "GDPR compliance in Dynamics 365 Customer Service Insights"
description: "Summary of capabilities for handling GDPR Data Subject Requests (DSR) for data used in Dynamics 365 Customer Service Insights"
keywords: ""
ms.date: 4/30/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# GDPR compliance in Customer Service Insights

The GDPR gives people (known in the GDPR as data subjects) specific rights to their personal data, including the ability to: obtain copies of personal data, request corrections or deletions, receive personal data in an electronic format so it can be moved to another controller, or to restrict processing of personal data. 

A formal request by a data subject to a controller to take an action on their personal data is called a Data Subject Request (DSR). [Learn more about DSR](https://docs.microsoft.com/microsoft-365/compliance/gdpr-dsr-azure).

Dynamics 365 Customer Service Insights includes capabilities to help you fulfill your obligations to data subjects when they exercise their rights to manage their personal data.

See these articles for more information:

* [Respond to discovery requests from data subjects](gdpr-discovery.md)
* [Export data to respond to requests for copies of personal data](gdpr-export.md)
* [Respond to requests to delete personal data](gdpr-delete.md)

## A note about requests to rectify personal data
If a data subject asks you to rectify or make changes to their personal data that resides in your organization, you and your organization must determine if it’s appropriate to honor the request. Rectifying the data might include taking actions such as editing, redacting, or removing personal data.

You use Azure Active Directory to manage Dynamics 365 Customer Service Insights users' identities. Organizations manage DSR rectify requests, including limited editing features, per the nature of a given Microsoft service. As a data processor, Microsoft doesn't offer the ability to correct system-generated logs because these logs reflect factual activities and constitute a historical record of events within Microsoft services. 


