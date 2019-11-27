---
title: "Permissions | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 11/27/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 83200632-a36b-4401-ba41-952e5b43f939
caps.latest.revision: 31
author: m-hartmann
ms.author: mhart
manager: shellyha
---
# Permissions

The **Permissions** page is where you'll set up roles and permissions for using Customer Insights across your organization. Customer Insights includes three types of roles.

| Role | Capabilities available under this role |
|---------|---------|
| Viewer | <ul><li>Explore insights and segments within the **Home** and **Segments** pages.</li><li>Search and filter customer profiles using the **Customers** page. (Note: Data fields should first be indexed as searchable by your administrator.)</li><li>Explore and export entities using the **Entities** page.</li> <li>View the status of system processes  using the **System** page.</li> <li>Export  segments from the **Segments** page to either a .csv file or to a Dynamics 365 Sales destination. (Note: Dynamics 365 Sales destinations should first be defined by your administrator.)</li><li>Install and use the **Power BI Customer Insights** dashboard to seek insights on your customers.</li></ul> |
| Contributor | <ul><li>All that is available to the Viewer.</li>AND<br /><li>Load and transform data using the **Data Sources** page.</li><li> Complete the *Data Unification* sections (**Map**, **Match**, and **Merge**) which result in the unified customer profile entity.</li> <li>Define **Relationships** and **Activities**.</li> <li>Create segments using the **Segment Builder** page.</li> <li>Create measures using the **Measures** page.</li> <li>Enrich customer profiles with Microsoft Graph data using the **Enrichment** page.</li></ul> |
| Administrator | <ul><li>All that is available to the Contributor.</li>AND<br /><li> Change settings on the **System** page, including the working language and refresh schedules for your system processes .</li> <li>View and add permissions using the **Permissions** page.</li> <li>Set Search and Filter definitions for the Customers page using the **Search & Filter Index** page (accessible via the **Customers** page).</li> <li>Define Dynamics 365 Sales segment destinations using the **Segment Export** page.</li><li>Install and use the **Customer Card Add-in**.</li> <li>Add and use the **Power Apps connector** to create apps with Customer Insights data.</li></ul> |

## Add roles and permissions

On the **Permissions** page, select **Add**. This opens the **Add permissions** pane.

> [!NOTE]
> Strings for roles are not localized. No matter what language you have selected, they will appear as "Admin", "Viewer", or "Contributor".

In the **Select** field, find the user whose permissions you want to adjust. Choose a **Role** to assign to that user.

> [!div class="mx-imgBorder"]
> ![Enter a name](media/permissions-roles.png "Enter a name")

Select **Save** in the lower-right corner of the pane. The current work instance will automatically be shared with the user whose permissions you have changed. This user will be able to enter the Customer Insights app and perform actions according to their specified role.

## View current permissions

After selecting **Save**, you can use the **Permissions** page to see what role assignments are currently active.

> [!div class="mx-imgBorder"]
> ![Permissions](media/permissions.png "Permissions")

Let's explore this page:

- The **Type** column specifies a single user, group, or application. Currently, Customer Insights supports only individual users, but in the future it will also support groups and applications that can connect to Customer Insights via APIs.
- Roles are specified under the **Role** column.
- Use the search field at the top of the page to locate specific users.
- You can click any column title to sort the results by that column's value.

## Filter permissions by role

At the top of the **Permissions** page, select **Filter** to open the **Filter** pane. Use this to filter the results on the page by role.

> [!div class="mx-imgBorder"]
> ![Permissions filter](media/permissions-filter.png "Permissions filter")

## View current number of users per role

At the top of the **Permissions** page, select **Roles** to open the **Roles** pane. Use this to see at a glance how many users are assigned to each role.

> [!div class="mx-imgBorder"]
> ![Number of users per role](media/permissions-roles2.png "Number of users per role")
