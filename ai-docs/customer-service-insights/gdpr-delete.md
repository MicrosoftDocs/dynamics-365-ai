---
title: "Responding to GDPR Data Subject Delete Requests for Dynamics 365 Customer Service Insights"
description: "Learn how to respond​ to GDPR Data Subject Delete Requests for Dynamics 365 Customer Service Insights."
keywords: ""
ms.date: 4/23/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Responding to GDPR data subject delete requests for Dynamics 365 Customer Service Insights

The “right to erasure” by the removal of personal data from an organization’s customer data is a key protection in the General Data Protection Regulation (GDPR). Removing personal data includes removing all personal data and system-generated logs, except audit log information.

## Manage delete requests

Dynamics 365 Customer Service Insights offers the following experiences to delete personal data for a specific user:

* Delete customer data (Tenant admin)
* Delete customer data (Self)

### Delete customer data (Tenant admin)

A tenant administrator can follow these steps to delete data:

1. Send email to ccinsightadmins@microsoft.com specifying the user’s Azure Active Directory (Azure AD) objectId in the request.

    An administrator from the Dynamics 365 Customer Service Insights team will send an email to the address registered in the Azure AD user account, asking for confirmation to delete data.
2. Acknowledge the confirmation to delete the data and receive a confirmation that the data has been deleted.

### Delete customer data – Telemetry (Tenant admin)

A tenant administrator can follow these steps to delete data:

1. Sign in to the [Azure management portal](https://ms.portal.azure.com).

2. Navigate to [https://portal.azure.com/?feature.usorIntimite=true#blade/Microsoft_Azure_Policy/PolicyMenuBlade/Privacy](https://portal.azure.com/?feature.usorIntimite=true#blade/Microsoft_Azure_Policy/PolicyMenuBlade/Privacy) to open the Privacy blade.

    > [!div class="mx-imgBorder"]
    ![Privacy blade](media/gdpr-export-1.png)

3. Select **Go to Azure AD to delete user**.

4. Select the user that you want to delete. 

    > [!div class="mx-imgBorder"]
    ![User list](media/gdpr-delete1.png)

5. Select **Delete**.

    > [!div class="mx-imgBorder"]
    ![Delete control](media/gdpr-delete2.png)

### Delete customer data (Self)

You can follow these steps to delete data from Customer Service Insights:

1. Navigate to [https://csi.ai.dynamics.com/](https://csi.ai.dynamics.com/).

2. Select the **Workspaces** icon on the Customer Service Insights title bar to open the **My workspaces** pane.

3. Hover over the workspace you want to delete to display the **Delete** icon, and then select the icon.

   ![Delete workspace](media/delete-workspace.png)
