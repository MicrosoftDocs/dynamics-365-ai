---
title: title: "Respond to GDPR Data Subject Discovery Requests (DSR) for Dynamics 365 Customer Service Insights"
description: "Find resources containing personal data to respond to GDPR discovery requests for Dynamics 365 Customer Service Insights"
keywords: ""
ms.date: 4/30/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Respond to GDPR Data Subject Discovery Requests (DSR) for Dynamics 365 Customer Service Insights

The first step in responding to a Data Subject Discovery Request (DSR) is finding personal data that is the subject of the request. This step helps you determine whether a DSR meets your organization's requirements for honoring or declining a DSR request. For example, after finding and reviewing the personal data that is the subject of the request, you may determine that the request doesn’t meet your organization’s requirements because it may adversely affect the rights and freedoms of others.

Below is a summary of the types of Dynamics 365 Customer Service Insights resources that contain personal data for a specific user.

Resources containing personal data | Purpose
---------------------------------- | -------
System-generated logs | Telemetry that captures system events and history.
System-supporting data | Supporting data for services, including user license information and user mapping to workspaces and regions.
User jobs | Details of provisioning and refreshing workspaces that are not seen by the user.
User AI insights | Temporary AI insights calculation results based on user data. The data is kept for one day. New data is generated during a refresh operation.
Aggregated usage telemetry | Data used to determine service usage for service operations management.
