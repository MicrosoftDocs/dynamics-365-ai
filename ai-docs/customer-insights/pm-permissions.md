---
title: "Permissions | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 04/29/2019
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
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
---
# Permissions

The **Permissions** page is where you can set up roles and permissions for using Customer Insights across the organization. Customer Insights includes three types of roles. 

|Role  |Capabilities available under this role  |
|---------|---------|
|Viewer     | <ul><li>Explore insights and segments within the **Home** and **Segments** pages.</li><li>Search and filter customer profiles using the **Customers** page. (Note: Fields in your data should first be indexed as searchable by your administrator.)</li><li>Explore as well as export entities using the **Entities** page.</li> <li>View system processes status using the **System** page.</li> <li>Exporting a segment from the **Segments** page to either a CSV file or to a Dynamics 365 Sales destination. (Note: Dynamics 365 Sales destinations should first be defined by your administrator.)</li><li>Install and use the **Power BI Customer Insights** dashboard to solicit insights on your customers.</li></ul>   |
|Contributor     | <ul><li>All that is available to the Viewer.</li>AND<br /><li>Load data into the system (and transform it) using the Data Sources page.</li><li> Complete the *Data Unification* sections: **Map**, **Match**, and **Merge** that result in the unified customer profile entity.</li> <li>Define **Relationships** and **Activities**.</li> <li>Create segments using the **Segment Builder** page.</li> <li>Create measures using the **Measures** page.</li> <li>Enrich customer profiles with Microsoft Graph data using the **Enrichment** page.</li></ul> |
|Administrator     | <ul><li>All that is available to the Contributor.</li> AND<br /><li> Change settings on the **System** page, including setting refresh schedules for your system processes, change language, etc. </li> <li>View and add permissions using the **Permissions** page.</li> <li>Set Search and Filter definitions for the Customers page using the **Search & Filter Index** page (accessible via the **Customers** page).</li> <li>Define Dynamics 365 Sales segment destinations using the **Segment Export** page.</li><li>Install and use the **Customer Card Add-in**.</li> <li>Add the **PowerApps connector** and create an app with Customer Insights data through it.</li></ul>     |
 
## Add roles and permissions

On the **Permissions** page, select **Add**. That opens the pane (shown on the right in the following example) where you should first choose a role. 

> [!NOTE]
> The strings for roles are not localized. No matter what language, they will show up as "Admin", "Viewer", or "Contributor".

> [!div class="mx-imgBorder"] 
> ![Add permissions](media/add-permissions.png "Add permissions")
 
Then, find the person to whom you want to give that permission. Enter this person's name in the **Select** field.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles.png "Enter a name")

Lastly, select **Save** in the lower-right corner of the pane. The instance that you are using will automatically be shared with the user you have defined the permissions for. This user will be able to enter the Customer Insights app and perform actions according to the role that you have specified.
 
## View current permissions

After selecting **Save**, you can use the **Permissions** page to explore all the permissions that are currently active.

> [!div class="mx-imgBorder"] 
> ![Permissions](media/permissions.png "Permissions")

Let's explore this page:

- The **Type** column specifies a single member, group, or application. Currently, Customer Insights supports only individual users, but in the future it will also support groups and applications that can connect to Customer Insights via APIs.
- The roles are specified under the **Roles** column.
- You can also look for a specific person by entering a name in the search field.
- You can sort the results by each of the columns.   

## Filter permissions by a role

At the top of the **Permissions** page, select **Filter** to open the **Filter** pane. Then, choose whether to filter the permissions by the Contributor, Reader, or Admin roles.

> [!div class="mx-imgBorder"] 
> ![Permissions filter](media/permissions-filter.png "Permissions filter")

### View current number of users per role

At the top of the **Permissions** page, select **Roles** to open the **Roles** pane. Use this pane to view the number of users per role.

> [!div class="mx-imgBorder"] 
> ![Number of users per role](media/permissions-roles2.png "Number of users per role")
