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

[add roles table]

[replace with permissions 1]:
 ![permissions.png](media/permissions.png)
 
- **Adding Roles and Permissions** 
This is done via the **Add Permissions** panel that can be accessed via  **Add** at the top of the permissions page:

 ![add-permissions.png](media/add-permissions.png)
 
Once the panel is opened, first you will need to find the **person, group, or application** to which you want to give the permission. Type a name in the **Name field** as shown below. As mentioned, beyond people you can also give permissions to applications, and these will connect to Customer 360 via our APIs.

[Permissions2]

Then, choose a role for that person/group/application as shown below:

 ![permissions-roles.png](media/permissions-roles.png)
 
 Lastly, hit **Save** in the bottom right corner of the panel.
 
- **Viewing current permissions**: After hitting save you can view all the permissions that were given in this page:

[replace with permissions 1]:
 ![permissions.png](media/permissions.png)

Let's explore this screen:

- The **Type** column specifies whether it's a single member or a group
- A role is specified under the **Roles** column
- You can also look for a specific person, group or application by typing it's name in the search field:
[?]

- Lastly, you can sort the results by each of the columns by clicking on the arrow icon next to the column name:  
[permissions4]

- **Filtering Permissions by a Role**: This can be achieved by opening the **Filter** panel through **Filter** at the top of the permissions page, and choosing whether to filter the permissions by the ***Administrator***, ***Contributor*** or ***Reader*** roles.

![permissions-filter.png](media/permissions-filter.png)

- **Viewing current number of users per role:** This can be done via the **Roles** panel that can be accessed via **Roles** at the top of the permissions page:
[permissions 3]
