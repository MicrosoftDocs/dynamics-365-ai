---
title: "Data retention and deletion policy for call insights | MicrosoftDocs"
description: "Data retention and deletion policy for call insights"
ms.date: 04/20/2020
ms.service: dynamics-365-ai
ms.custom: 
ms.topic: article
author: lalexms
ms.author: laalexan
manager: shujoshi 

---

# Data retention and deletion through Privacy

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

>[!IMPORTANT]
>This feature is intended to help supervisors enhance their team’s performance. This feature is not intended for use in making, and should not be used to make, decisions that affect the employment of an employee or group of employees, including compensation, rewards, seniority, or other rights or entitlements. Customers are solely responsible for using Dynamics 365, this feature, and any associated feature or service in compliance with all applicable laws, including laws relating to accessing individual employee analytics and monitoring, recording, and storing communications with end users. This also includes adequately notifying end users that their communications with sales persons may be monitored, recorded, or stored and, as required by applicable laws, obtaining consent from end users before using the feature with them. Customers are also encouraged to have a mechanism in place to inform their sales persons that their communications with end users may be monitored, recorded, or stored.

When you configure call insights, call recordings of agents are processed and analyzed to provide necessary insights such as overall customer sentiments, sentiment trends, and identify keywords that customers have used during calls. Call insights provides the following options to configure your retention period:

-	[Retention policy](#retention-policy)

-	[Delete agent data](#delete-agent-data)

## Retention Policy

Retention policy allows you to determine how long you want to keep the analyzed call recording data in call insights by specifying a time limit. When you specify a retention time limit, the feature retains the call recording data for the specified time limit. Call insights deletes the data when the time limit is reached. 

For example, retention time limit is set 30 days. At any given time, call insights retains the call data from the time it is analyzed to 30 days. On the 31st day, the application deletes the analyzed call data.

To configure the retention policy:

1.	Review the perquisites. To learn more, see [Prerequisites to set up call insights](ci-admin-prereqs.md).

2.	Open **Call insights (Preview)**. 

3.	Select the **Settings** icon on the top-right of the page and then select **Settings**.

    > [!div class="mx-imgBorder"]
    > ![Select settings option](media/ci-app-admin-select-settings.png "Select settings option")
 
4.	On the **Settings** page, select **Privacy**. 
    
    > [!div class="mx-imgBorder"]
    > ![Select privacy option](media/ci-app-admin-settings-privacy.png "Select privacy option")
 
5.	In the **Retention policy** section, select the drop-down and choose how many days you want to retain the analyzed data. You have the following options to choose: **30 days**, **90 days**, **1 year**, or **Always**.
    
    > [!div class="mx-imgBorder"]
    > ![Select data retention time](media/ci-app-admin-select-retention-policy.png "Select data retention time")
 
6.	Select **Save**.

Retention policy configuration is saved, and the analyzed call recording data will be retained until the selected option.

## Delete agent data

You can delete an agent's data when the agent no longer reports to you, moves to another team, leaves your organization, or the agent requests to delete their data. This data includes the agent’s statistics and call history. 

To delete an agent’s data that you don’t want to see in your insights:

1.	Review the prerequisites. To learn more, see [Prerequisites to set up call insights](ci-admin-prereqs.md).

2.	Open **call insights** in Customer Service Insights. 

3.	Select the **Settings** icon on the top-right of the page and then select **Settings**.

    > [!div class="mx-imgBorder"]
    > ![Select settings option](media/ci-app-admin-select-settings.png "Select settings option")
 
4.	On the **Settings** page, select **Privacy**. 

    > [!div class="mx-imgBorder"]
    > ![Select privacy option](media/ci-app-admin-settings-privacy.png "Select privacy option")
 
5.	In the **Delete agent data** section, select the agent for whom you want to delete the data, then select **Delete data**.

    > [!NOTE]
    > You can also you use the search option to find and select the seller. 

    In this example, we are deleting the agent Robin Counts’s data.

    > [!div class="mx-imgBorder"]
    > ![Select an agent to delete data](media/ci-app-admin-select-agent-delete.png "Select an agent to delete data")

6.	On the confirmation message, select **Delete**.

    > [!div class="mx-imgBorder"]
    > ![Confirmation message to delete data](media/ci-app-admin-message-agent-data-delete.png "Confirmation message to delete data")

    The selected agent data is deleted from call insights.

    > [!div class="mx-imgBorder"]
    > ![Agent data deleted](media/ci-app-admin-agent-delete-deleted.png "Agent data deleted")

To learn more on Microsoft Dynamics 365 and GDPR, see [Microsoft Dynamics 365 and GDPR](https://docs.microsoft.com/dynamics365/get-started/gdpr/index).

### See also

[Overview of call insights](ci-overview.md)

[Prerequisites to use call insights](ci-admin-prereqs.md)

[First-run setup experience](ci-admin-fre-setup.md)

[Configure call insights to connect call data](ci-admin-config-call-data.md)

[Configure keywords and products to track](ci-admin-config-keywords-products.md)

[Connect to Dynamics 365 Customer Service environment](ci-connect-customer-service-env.md)
