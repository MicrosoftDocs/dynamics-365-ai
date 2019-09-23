---
title: "Data retention and deletion policy for Dynamics 365 Sales Insights application | MicrosoftDocs"
description: "Data retention and deletion policy for Dynamics 365 Sales Insights application"
ms.date: 07/31/2018
ms.service: crm-online
ms.custom: 
ms.topic: article
applies_to:
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: c85b26ab-0150-454f-8767-6aed448529bc
author: udaykirang
ms.author: udag
manager: shujoshi
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
caps.latest.revision: 01
topic-status: Drafting
---

# Data retention and deletion through Privacy

When you configure conversation intelligence, sales call recordings of sales reps are processed and analyzed to provide necessary insights such as overall customer sentiments, sentiment trends, and identify keywords that customers have used during calls. Sales Insights application provides the following options to configure your retention period:

-	[Retention policy](#retention-policy)

-	[Delete seller data](#delete-seller-data)

## Retention Policy

Retention policy allows you to determine how long you want to keep the analyzed call recording data in the Sales Insights application by specifying a time limit. When you specify a retention time limit, the application retains the call recording data for the specified time limit. The application deletes the data when the time limit is reached. 

For example, retention time limit is set 30 days. At any given time, application retains the call data from the time it is analyzed to 30 days. On the 31st day, the application deletes the analyzed call data.

To configure the retention policy:

1.	Review the perquisites. To learn more, see [Prerequisites to setup Sales Insights application](prereq-sales-insights-app.md).

2.	Open **Dynamics 365 Sales Insights** application. 

3.	Select the **Settings** icon on the top-right of the page and then select **Settings**.

    > [!div class="mx-imgBorder"]
    > ![Select settings option](media/si-app-admin-select-settings.png "Select settings option")
 
4.	On the **Settings** page, select **Privacy**. 
    
    > [!div class="mx-imgBorder"]
    > ![Select privacy option](media/si-app-admin-settings-privacy.png "Select privacy option")
 
5.	In the **Retention policy** section, select the drop-down and choose how many days you want to retain the analyzed data. You have the following options to choose: **30 days**, **1 year**, or **Always**.
    
    > [!div class="mx-imgBorder"]
    > ![Select data retention time](media/si-app-admin-select-retention-policy.png "Select data retention time")
 
6.	Select **Save**.

Retention policy configuration is saved, and the analyzed call recording data will be retained until the selected option.

## Delete seller data

You can delete seller’s data when a seller is not reporting to you, moved to another team, leaving your organization, or seller requests to delete his data. This data includes the seller’s statistics and call history. To delete a seller’s data that you don’t want to see in your insights:

1.	Review the perquisites. To learn more, see [Prerequisites to setup Sales Insights application](prereq-sales-insights-app.md).

2.	Open **Dynamics 365 Sales Insights** application. 

3.	Select the **Settings** icon on the top-right of the page and then select **Settings**.

    > [!div class="mx-imgBorder"]
    > ![Select settings option](media/si-app-admin-select-settings.png "Select settings option")
 
4.	On the **Settings** page, select **Privacy**. 

    > [!div class="mx-imgBorder"]
    > ![Select privacy option](media/si-app-admin-settings-privacy.png "Select privacy option")
 
5.	In the **Delete seller data** section, select the seller for whom you want to delete the data and then select **Delete data**.

    > [!NOTE]
    > You can also you use the search option to find and select the seller. 

    In this example we are deleting the seller Robin Counts’s data.

    > [!div class="mx-imgBorder"]
    > ![Select a seller to delete data](media/si-app-admin-select-seller-delete.png "Select a seller to delete data")

6.	On the confirmation message, select **Delete**.

    > [!div class="mx-imgBorder"]
    > ![Confirmation message to delete data](media/si-app-admin-message-seller-data-delete.png "Confirmation message to delete data")

    The selected seller data is deleted from the Sales Insights application.

    > [!div class="mx-imgBorder"]
    > ![Seller data deleted](media/si-app-admin-seller-delete-deleted.png "Seller data deleted")

To learn more on Microsoft Dynamics 365 and GDPR, see [Microsoft Dynamics 365 for Customer Engagement apps and GDPR](https://docs.microsoft.com/en-us/dynamics365/get-started/gdpr/index).

### See also

[Introduction to administer Sales Insights application](intro-admin-guide-sales-insights.md#administer-sales-insights-application)

[Prerequisites to use Sales Insights application](prereq-sales-insights-app.md)