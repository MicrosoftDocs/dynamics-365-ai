---
title: "Permissions | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 02/21/2019
ms.reviewer: ""
ms.service: "dynamics-365-ai"
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
|Contributor     | <ul><li>Complete **Data Manager**: **Data Sources** </li><li>Complete **Configure Data** sections: **Map**, **Match**, **Merge**, **Relationships**, **Activities**, etc </li><li>View **Home** and **Segments** pages </li><li>Create segments in the **Segment Builder** page  </li></ul> |
|Administrator     | <ul><li>All that is available to the Contributor</li></ul>AND<ul><li>Change settings in the **Settings** page</li><li>View and add permissions in the **Permissions** page</li><li>Set Search and Filter definitions for the **Profiles** page using the **Search, Sort and Filter** page   </li></ul>     |
 
## Add roles and permissions

On the **Permissions** page, select **Add** to add permissions and roles to users.

> [!div class="mx-imgBorder"] 
> ![](media/add-permissions.png "Add permissions")

First, decide on the role.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles.png "Enter a name")
 
Then, find the person to whom you want to give that permission. Type this person's name in the **Select** field.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles.png "Enter a name")

Lastly, select **Save** in the bottom-right corner of the panel. The instance that you are using will be automatically shared with the user you have defined the permission for. This user will be able to enter the Customer Insights app and perform actions according to the role that you have specified.
 
## View current permissions

After selecting **Save**, you can utilize the **Permissions** page to explore all the permissions currently active.

> [!div class="mx-imgBorder"] 
> ![](media/permissions.png "Permissions")

Let's explore this page:

- The **Type** column specifies whether it's a single member, a group, or an application. Currently, Customer Insights supports only individual users but in the future it will also support groups and applications that will connect to Customer Insights via our APIs.
- The roles are specified under the **Roles** column.
- You can also look for a specific person by typing a name in the search field.
- You can sort the results by each of the columns.   

## Filter permissions by a role

At the top of the **Permissions** page, select **Filter** to open the **Filter** panel. Then, choose whether to filter the permissions by the Administrator, Contributor, or Reader roles.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-filter.png "Permissions filter")

### View current number of users per role

At the top of the **Permissions** page, select **Roles** to open the **Roles** panel. Then use this panel to view the number of users per role.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles2.png "Roles")
