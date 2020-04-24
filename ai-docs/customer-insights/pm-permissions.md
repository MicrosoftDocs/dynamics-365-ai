---
title: "User permissions in Dynamics 365 Customer Insights | Microsoft Docs"
description: "Learn about permissions and user roles in Dynamics 365 Customer Insights."
ms.date: 04/17/2020
ms.reviewer: nimagen
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# User permissions

The **Permissions** page is where you'll set up roles and permissions for using Dynamics 365 Customer Insights across your organization. Customer Insights includes three types of roles.

## Viewer

- Explore insights and segments within the **Home** and **Segments** pages.
- Search and filter customer profiles using the **Customers** page. (Note: Data fields should first be indexed as searchable by your administrator.)
- View and explore the **Enrichment** page.
- Explore and export entities using the **Entities** page.
- View the status of system processes  using the **System** page.
- Export segments from the **Segments** page to either a .csv file or to a Dynamics 365 Sales destination. (Note: Dynamics 365 Sales destinations should first be defined by your administrator.)
- Install and use the **Power BI Customer Insights** dashboard to seek insights on your customers.

## Contributor

- All permissions available to the Viewer.
- Load and transform data using the **Data Sources** page.
- Complete the *Data Unification* sections (**Map**, **Match**, and **Merge**) which result in the unified customer profile entity.
- Define **Relationships** and **Activities**.
- Create segments using the **Segment Builder** page.
- Create measures using the **Measures** page.
- Manage configuration and enrich customer profiles on the **Enrichment** page (for 1st party enrichments only).

## Administrator

- All permissions available to the Contributor.
- Change settings on the **System** page, including the working language and refresh schedules for your system processes.
- View and add permissions using the **Permissions** page.
- Set Search and Filter definitions for the Customers page using the **Search & Filter Index** page (accessible via the **Customers** page)
- Define Dynamics 365 Sales segment destinations using the **Segment Export** page.
- Manage configuration and enrich customer profiles on the **Enrichment** page (for all enrichments).
- Install and use the **Customer Card Add-in**.
- Add and use the **Power Apps connector** to create apps with Customer Insights data.

## Assign roles and permissions

1. On the **Permissions** page, select **Add** to open the **Add permissions** pane.

2. In the **Select** field, find the user or group whose permissions you want to adjust. Choose a **Role** to assign to that user or group.

3. Select **Save** in the lower-right corner of the pane. The current work instance will automatically be shared with the user or members of the group whose permissions you've changed. Users can access the Customer Insights app and perform actions according to their specified role.

## View current permissions

Use the **Permissions** page to see what role assignments are currently active.

- The **Type** column specifies a single user, group, or application. Currently, Customer Insights supports individual users and groups. 
- Roles are specified under the **Role** column.
- Use the search field at the top of the page to locate specific users.
- You can select any column title to sort the results by that column's value.

## View and filter permissions by role

On **Permissions** page, select **Filter** to open the **Filter** pane. Here you can filter the results on the page by role.

On the **Permissions** page, select **Roles** to open the **Roles** pane. Here you can see at a glance how many users are assigned to each role.
