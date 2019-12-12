---
title: "Permissions | Microsoft Docs"
description: "Learn about permissions and user roles in Dynamics 365 Customer Insights."
ms.date: 12/02/2019
ms.reviewer: nimagen
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Permissions

The **Permissions** page is where you'll set up roles and permissions for using Dynamics 365 Customer Insights across your organization. Customer Insights includes three types of roles.

## Viewer

- Explore insights and segments within the **Home** and **Segments** pages.
- Search and filter customer profiles using the **Customers** page. (Note: Data fields should first be indexed as searchable by your administrator.)
- Explore and export entities using the **Entities** page.
- View the status of system processes  using the **System** page.
- Export  segments from the **Segments** page to either a .csv file or to a Dynamics 365 Sales destination. (Note: Dynamics 365 Sales destinations should first be defined by your administrator.)
- Install and use the **Power BI Customer Insights** dashboard to seek insights on your customers.

## Contributor

- All permissions available to the Viewer.
- Load and transform data using the **Data Sources** page.
- Complete the *Data Unification* sections (**Map**, **Match**, and **Merge**) which result in the unified customer profile entity.
- Define **Relationships** and **Activities**.
- Create segments using the **Segment Builder** page.
- Create measures using the **Measures** page.
- Enrich customer profiles with Microsoft Graph data using the **Enrichment** page.

## Administrator

- All permissions available to the Contributor.
- Change settings on the **System** page, including the working language and refresh schedules for your system processes.
- View and add permissions using the **Permissions** page.
- Set Search and Filter definitions for the Customers page using the **Search & Filter Index** page (accessible via the **Customers** page)
- Define Dynamics 365 Sales segment destinations using the **Segment Export** page.
- Install and use the **Customer Card Add-in**.
- Add and use the **Power Apps connector** to create apps with Customer Insights data.

## Assign roles and permissions

1. On the **Permissions** page, select **Add**. This opens the **Add permissions** pane.

2. In the **Select** field, find the user whose permissions you want to adjust. Choose a **Role** to assign to that user.

   > [!div class="mx-imgBorder"]
   > ![Enter a name](media/permissions-roles.png "Enter a name")

3. Select **Save** in the lower-right corner of the pane. The current work instance will automatically be shared with the user whose permissions you have changed. This user will be able to enter the Customer Insights app and perform actions according to their specified role.

## View current permissions

Use the **Permissions** page to see what role assignments are currently active.

- The **Type** column specifies a single user, group, or application. Currently, Customer Insights supports only individual users, but in the future it will also support groups and applications that can connect to Customer Insights via APIs.
- Roles are specified under the **Role** column.
- Use the search field at the top of the page to locate specific users.
- You can select any column title to sort the results by that column's value.

## View and filter permissions by role

On **Permissions** page, select **Filter** to open the **Filter** pane. Use this to filter the results on the page by role.

On the **Permissions** page, select **Roles** to open the **Roles** pane. Use this to see at a glance how many users are assigned to each role.
