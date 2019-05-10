---
title: "Improve data quality by cleansing support case titles"
description: "Learn how to improve data quality by cleansing support case titles in Virtual Agent for Customer Service."
keywords: ""
ms.date: 05/10/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Improve data quality by cleansing support case titles

If you have connected Dynamics 365 Virtual Agent for Customer Service to your existing Dynamics 365 customer service data, Virtual Agent uses the data in its analytics dashboards. However, the dashboards can be misleading if the customer service case titles include extraneous information. For example, support case titles may include information such as product name, case status, or ticket number tags.

You can improve the quality of the results displayed in analytics dashboards by cleansing your support case titles. Virtual Agent will then disregard the extraneous information when support cases are grouped into topics.

## To cleanse support case titles

1. Select the **Settings** button on the Virtual Agent title bar and then select **Data Cleansing** to display the Case title cleansing pane of the Settings window.

   > ![Display cleansing pane](media/case-title-cleansing.png)

2. Select the check box next to **I want to cleanse my case titles**. Specify any delimiter characters you use to separate tags from each other or from the issue summary, and whether you place tags before or after the summary, or both. Then select **Save**.

   > ![Case Titles toggle](media/cleanse-titles.png)

The settings take effect when you refresh the workspace.
