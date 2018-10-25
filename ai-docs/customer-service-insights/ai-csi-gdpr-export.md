---
title: "Responding to GDPR Data Subject Export Requests for Dynamics 365 AI for Customer Service"
description: "Learn how to respond​ to GDPR Data Subject Export Requests for Dynamics 365 AI for Customer Service."
keywords: ""
ms.date: 10/24/2018
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Responding to GDPR Data Subject Export Requests for Dynamics 365 AI for Customer Service

As part of our commitment to partner with you on your journey to the General Data Protection Regulation (GDPR), we’ve developed documentation to help you prepare. The documentation not only describes what we’re doing to prepare for the GDPR but also shares examples of steps you can take today with Microsoft to support GDPR compliance when using Dynamics 365 AI for Customer Service.

## Manage Export requests

The right of data portability allows a data subject to request a copy of their personal data in an electronic format (that’s a “structured, commonly used, machine readable, and interoperable format”) that may be transmitted to another data controller.

Dynamics 365 AI for Customer Service Insights offers the following experiences to find or export personal data for a specific user:

* Export customer data – Telemetry (Tenant admin)
* Export customer data – Other (Tenant admin)
* Export customer data – Other (Self)

### Export customer data – Telemetry (Tenant admin)

A tenant administrator can follow these steps to export data:

1. Log into the [Azure management portal](https://ms.portal.azure.com).
2. Navigate to [https://portal.azure.com/?feature.usorIntimite=true#blade/Microsoft_Azure_Policy/PolicyMenuBlade/Privacy](https://portal.azure.com/?feature.usorIntimite=true#blade/Microsoft_Azure_Policy/PolicyMenuBlade/Privacy) to open the Privacy blade.

    ![Privacy blade](media/ai-csi-gdpr-export1.png)

3. Create a request to export and delete user data by providing following details:

    ![Request details](media/ai-csi-gdpr-export2.png)

After the export runs successfully, you will see the data in your storage container.

### Export customer data – Other (Tenant admin)

A tenant administrator can follow these steps to export data:

1. Send email to [ccinsightadmins@microsoft.com](ccinsightadmins@microsoft.com) specifying the user’s AAD objectId in the request.

    An administrator from the Dynamics 365 AI for Customer Service Insights team will send an email to the address registered in the AAD user account, asking for confirmation to export data.
2. Acknowledge the confirmation to export the data and make it available to the requestor.

### Export customer data – Other (Self)

You can follow these steps to export data from a chart on an AI for Customer Service Insights dashboard:

1. Navigate to [https://csi.ai.dynamics.com/](https://csi.ai.dynamics.com/).
2. Click on the elipses in the upper right corner of the chart, and then click **Export data**.

    ![Export data](media/ai-csi-gdpr-export3.png)
