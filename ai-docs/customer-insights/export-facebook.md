---
title: "Export Customer Insights data to Dynamics 365 Marketing | Microsoft Docs"
description: "Learn how to configure the connection to Facebook Ads Manager."
ms.date: 05/18/2020
ms.reviewer: philk
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Facebook Ads Manager
Create custom or lookalike audiences on Facebook with your unified customer profile data and use the audiences for your campaigns on Facebook and Instagram.

## Pre-requisites
-	You need to have a Facebook Ad Account which includes a Facebook Business Account
-	You need to be Administrator on the Facebook Ad Account

## Connect
1.	Go to **Admin** > **Export destinations**
2.	Under Facebook Ads Manager, select **Set up**
3.	Give your destination a recognizable name in the **Display name** field
4.	Click on the **Continue with Facebook** button to authenticate with Facebook
    - Several sequential pop windows will show up for the Facebook authentication 
    - Granting the **ads_management** permission to Customer Insights is a separate and additional step after the initial authentication
5.	After authentication is completed and permission is granted select the **Facebook Ads Account** that you want to work with. 
6.	Select an **existing Custom Audience** from the drop down, or create a new custom audience by selecting New custom Audience
7.	Provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox
8.	Select **Next** to start configuring the export

## Configure
1.	In the **Choose your key identifier field**, select **Email**, **Name and address**, or **Phone** to send to Facebook Ads Manager
2.	Map the corresponding attributes from your unified customer entity for the selected key identifier.
    > [TIP] 
    > The best chances for a match occur if you select **Email** as key identifier. Adding additional identifiers may increase the matching rate. 
3.	Select **Add attribute** to map additional attributes to send to Facebook Ads Manager
    - Attributes from Facebook Ads Manager are mapping to the following user friendly names
    - **FN** = **First Name**, **LN** = **Last Name**, **FI** = **First Initial**, **PHONE** = **Phone**, **GEN** = **Gender**, **DOB** = **Date of birth**, **ST** = **State**, **CT** = **City**, **ZIP** = **Postal code / Zip code**, **COUNTRY** = **Country / Region**
4.	Select the segments you want to export
5.	Select **Save**
    > [TIP] Read more about [**Audiences in Facebook Ads Manager**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494) and how to use them efficiently.

# Export
1.	Go to **Export destinations** tab to view your configured destinations 
2.	If you want to trigger the export manually **select** the ellipsis (...) after your destination and then choose the Export option to run the export for this specific destination
3.	The export is also running automatically with every scheduled refresh
