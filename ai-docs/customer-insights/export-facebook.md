---
title: "Export Customer Insights data to Dynamics 365 Marketing | Microsoft Docs"
description: "Learn how to configure the connection to Facebook Ads Manager."
ms.date: 06/05/2020
ms.reviewer: philk
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Connector for Facebook Ads Manager (preview)

Export segments of unified customer profiles to Facebook Ads Manager to create campaigns on Facebook and Instagram.

## Prerequisites

- You need to have a Facebook Ad Account which includes a Facebook Business Account.
- You need to be an administrator on the Facebook Ad Account.

## Connect to Facebook Ads Manager

1. Go to **Admin** > **Export destinations**.

1. Under **Facebook Ads Manager**, select **Set up**.

1. Give your export destination a recognizable name in the **Display name** field.

1. Select **Continue with Facebook** to sign in to your Facebook Ad Account.

1. Allow the **ads_management** permission to Customer Insights after authenticating with Facebook.

1. Select the **Facebook Ads Account** that you want to work with.

1. Select an **Existing custom audience** from the drop-down list or create a **New custom audience**. For more information, see [**Audiences in Facebook Ads Manager**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).

1. Select **I agree** to confirm the **Data privacy and compliance**.

1. Select **Next** to configure the export.

## Configure the connector

1. In the **Choose your key identifier field**, select **Email**, **Name and address**, or **Phone** to send to Facebook Ads Manager.

1. Map the corresponding attributes from your unified customer entity for the selected key identifier.
   > [TIP]
   > The best chances for a match occur if you select **Email** as key identifier. Adding additional identifiers may improve the matching.

1. Select **Add attribute** to map additional attributes to send to Facebook Ads Manager. Attributes from Facebook Ads Manager are mapping to the following user friendly names: 
    **FN** = **First Name**, **LN** = **Last Name**, **FI** = **First Initial**, **PHONE** = **Phone**, **GEN** = **Gender**, **DOB** = **Date of birth**, **ST** = **State**, **CT** = **City**, **ZIP** = **Postal code / Zip code**, **COUNTRY** = **Country / Region**

1. Select the segments you want to export.

1. Select **Save**.


# Export
1.	Go to **Export destinations** tab to view your configured destinations 
2.	If you want to trigger the export manually **select** the ellipsis (...) after your destination and then choose the Export option to run the export for this specific destination
3.	The export is also running automatically with every scheduled refresh
