---
title: "Permissions | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 03/26/2019
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

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The **Permissions** page is where you can set up roles and permissions for using Customer Insights across the organization. Customer Insights includes three types of roles. 

|Role  |Capabilities available under this role  |
|---------|---------|
|Viewer     | <ul><li>View **Home** and **Segments** pages </li></ul>       |
|Contributor     | <ul><li>Complete **Data Manager**: **Data Sources** </li><li>Complete **Configure Data** sections: **Map**, **Match**, **Merge**, **Relationships**, **Activities**, etc. </li><li>View **Home** and **Segments** pages </li><li>Create segments in the **Segment Builder** page  </li></ul> |
|Administrator     | <ul><li>All that is available to the Contributor</li></ul>AND<ul><li>Change settings on the **Settings** page</li><li>View and add permissions on the **Permissions** page</li><li>Set Search and Filter definitions for the **Profiles** page using the **Search, Sort and Filter** page   </li></ul>     |
 
## Add roles and permissions

On the **Permissions** page, select **Add**. That opens the pane (shown on the right in the following example) where you should first choose a role. 

>[!NOTE]
>The strings for roles are not localized. No matter what language, they will show up as "Admin", "Viewer", or "Contributor".

> [!div class="mx-imgBorder"] 
> ![](media/add-permissions.png "Add permissions")
 
Then, find the person to whom you want to give that permission. Enter this person's name in to the **Select** field.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles.png "Enter a name")

Lastly, select **Save** in the lower-right corner of the pane. The instance that you are using will automatically be shared with the user you have defined the permissions for. This user will be able to enter the Customer Insights app and perform actions according to the role that you have specified.
 
## View current permissions

After selecting **Save**, you can use the **Permissions** page to explore all the permissions that are currently active.

> [!div class="mx-imgBorder"] 
> ![](media/permissions.png "Permissions")

Let's explore this page:

- The **Type** column specifies a single member, a group, or an application. Currently, Customer Insights supports only individual users, but in the future it will also support groups and applications that can connect to Customer Insights via APIs.
- The roles are specified under the **Roles** column.
- You can also look for a specific person by entering a name in the search field.
- You can sort the results by each of the columns.   

## Filter permissions by a role

At the top of the **Permissions** page, select **Filter** to open the **Filter** pane. Then, choose whether to filter the permissions by the Contributor, Reader, or Admin roles.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-filter.png "Permissions filter")

### View current number of users per role

At the top of the **Permissions** page, select **Roles** to open the **Roles** pane. Use this pane to view the number of users per role.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles2.png "Roles")
