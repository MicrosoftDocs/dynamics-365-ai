---
title: "Export Customer Insights data to Dynamics 365 Marketing | Microsoft Docs"
description: "Learn how to configure the connection to SFTP."
ms.date: 05/18/2020
ms.reviewer: philk
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# SFTP 
Use your customer data in 3rd party applications by exporting them securely through our SFTP connector.

## Pre-requisites
-	Subscription (if needed) to the 3rd party application of your choice
-	Subscription or availability of a SFTP location of your choice

## Connect
1.	Go to **Admin** > **Export destinations**  
2.	Under SFTP, select **Set up**
3.	Give your destination a recognizable name in the **Display name** field.
4.	Provide a **Username**, **Password** and **Hostname** (example.com:1234/folderpath) for your SFTP account.
5.	Select **Verify** to test the connection.
6.	After successful verification, decide whether to export your data as **Zipped** or **Unzipped**, and with which **field delimiter**. 
7.	Provide your consent for **Data privacy and compliance** by selecting the I agree checkbox.
8.	Select **Next** to start configuring the export

## Configure
1.	Select the **customer attributes** to be exported
2.	You can choose one, several or all attributes depending what you want to export
3.	Select **Next**
4.	Select the segments you want to export
5.	Select **Save**

## Export
1.	Go to **Export destinations** tab to view your configured destinations 
2.	If you want to trigger the export manually **select** the ellipsis (...) after your destination and then choose the Export option to run the export for this specific destination
3.	The export is also running automatically with every scheduled refresh
