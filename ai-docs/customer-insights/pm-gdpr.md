---
title: "GDPR support | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/21/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# GDPR support

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Responding to GDPR data subject delete requests for Dynamics 365 Customer Insights 

The “right to erasure” by the removal of personal data from an organization’s customer data is a key protection in the General Data Protection Regulation (GDPR). Removing personal data includes removing all personal data and system-generated logs, except audit log information.

### Manage data subject delete requests

Dynamics 365 Customer Insights offers the following in-product experiences to delete personal data for a specific customer or Customer Insights user:

- Manage delete requests for customer data: The customer data in Customer Insights is ingested from original data sources external to Customer Insights and all GDPR delete requests need to be performed in the original data source.
- Manage delete requests for Customer Insights user data: The data for Customer Insights users is created by Customer Insights and all GDPR delete requests.

#### Manage delete requests for customer data

A Customer Insights admin can follow these steps to delete customer data:

1. Sign in to Dynamics 365 for Customer Insights
2. Navigate to the Data Sources page
3. For each data source in the list that contains customer data do the following:
   1. Select (...) under Action and then select **Refresh**.
   2. Check the status of the data source under Status. A check mark means refresh was successful. A warning triangle means something went wrong. If a Waning Triangle is displayed, please contact CustomerInsightsAdmins@micrsosoft.com.

> [!div class="mx-imgBorder"] 
> ![](media/gdpr-data-sources.png "Handling GDPR delete requests for customer data")

Handling GDPR delete requests for customer data

#### Manage delete requests for Customer Insights user data

A Customer Insights admin can follow these steps to delete Customer Insights user data:

1.	Sign in to Dynamics 365 Customer Insights.
2.	Navigate to the **Permissions** page.
3.	Check the checkbox for the user you want to delete.
4.	Select **Remove** in upper-left corner of the grid.

> [!div class="mx-imgBorder"] 
> ![](media/gdpr-permissions.png "Handling GDPR delete requests for Customer Insights user data")

Handling GDPR delete requests for Customer Insights user data

## Responding to GDPR data subject export requests for Dynamics 365 Customer Insights

As part of our commitment to partner with you on your journey to the General Data Protection Regulation (GDPR), we’ve developed documentation to help you prepare. The documentation not only describes what we’re doing to prepare for the GDPR but also shares examples of steps you can take today with Microsoft to support GDPR compliance when using Dynamics 365 Customer Insights.

### Manage export and view requests

The right of data portability allows a data subject to request a copy of their personal data in an electronic format (that’s a “structured, commonly used, machine readable, and interoperable format”) that may be transmitted to another data controller.

Dynamics 365 Customer Insights offers the following experiences to find or export personal data for a specific user:

- Export customer data (Tenant admin)
- Export Customer Insights user data (Tenant admin)
- Export Customer Insights user data – Telemetry (Tenant admin)

#### Export customer data (Tenant admin)

A tenant administrator can follow these steps to export data:

1.	Send an email to D365CI@micrsosoft.com specifying the customer’s email address in the request. An administrator from the Dynamics 365 Customer Insights team will send an email to the registered tenant admin email address, asking for confirmation to export data.
2.	Acknowledge the confirmation to export the data for requested customer.
3.	Receive the exported data through tenant admin email address.

#### Export Customer Insights user data (Tenant admin)

1.	Send an email to D365CI@micrsosoft.com specifying the users email address in the request. An administrator from the Dynamics 365 Customer Insights team will send an email to the registered tenant admin email address, asking for confirmation to export data
2.	Acknowledge the confirmation to export the data for requested user
3.	Receive the exported data through tenant admin email address

#### Export Customer Insights user data – Telemetry (Tenant admin)

1.	Send an email to D365CI@micrsosoft.com specifying the user’s email address in the request, and also specify that export is for user’s telemetry data. An administrator from the Dynamics 365 Customer Insights team will send an email to the registered tenant admin email address, asking for confirmation to export data.
2.	Acknowledge the confirmation to export the data for requested user.
3.	Receive the exported data through tenant admin email address.



