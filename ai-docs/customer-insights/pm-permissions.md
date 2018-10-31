---
title: "Permissions| MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/31/2018
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
robots: noindex,nofollow
---
# Permissions

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

The main administration page is the **Permissions** page where you can set up roles and permissions for using Customer 360 across your organization. As an administrator, the following roles are available for you to assign:

|Role  |Options available under this role  |
|---------|---------|
|Viewer     | <ul><li>View **Segments** page </li></ul>       |
|Contributor     | <ul><li>Complete **Data Manager**: **Get Data** </li><li>Complete **Configure Data** sections: **Map**, **Match**, **Merge** </li><li>View **Segments** page </li><li>Create segments in the **Segment Creation** page  </li></ul> |
|Administrator     | <ul><li>All that is available to the Contributor</li></ul>AND<ul><li>Change settings in the **Settings** page</li><li>View and add permissions in the **Permissions** page   </li></ul>     |
 
- **Adding Roles and Permissions** 
This is done via the **Add Permissions** panel that can be accessed via  **Add** at the top of the permissions page:

Replace with permissions final1:
 ![add-permissions.png](media/add-permissions.png)
 
Once the panel is opened, first you will need to find the person to which you want to give the permission. Type a name in the **Name field** as shown below.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles.png "Add permissions")

Then, choose a role for that person as shown below:

[missing permissions image]

Lastly, hit **Save** in the bottom right corner of the panel. Upon saving a permission, an instance will be automatically created for the user for whom you have defined the permission. This user will be able to enter the Customer 360 app and perfom actions according to the roles table that was specified above.
 
- **Viewing current permissions**: After hitting save you can view all the permissions that were given in this page:

> [!div class="mx-imgBorder"] 
> ![](media/permissions.png "Permissions")

Let's explore this screen:

- The **Type** column specifies whether it's a single member, a group, or an application (at this point Customer 360 supports only individual users)
- Roles are specified under the **Roles** column
- You can also look for a specific person, group or application by typing it's name in the search field:
[?]

- Lastly, you can sort the results by each of the columns by clicking on the arrow icon next to the column name:  
[permissions4]

- **Filtering Permissions by a Role**: This can be achieved by opening the **Filter** panel through **Filter** at the top of the permissions page, and choosing whether to filter the permissions by the ***Administrator***, ***Contributor*** or ***Reader*** roles.

![permissions-filter.png](media/permissions-filter.png)

- **Viewing current number of users per role:** This can be done via the **Roles** panel that can be accessed via **Roles** at the top of the permissions page:

> [!div class="mx-imgBorder"] 
> ![](media/permissions-roles2.png "Roles")
