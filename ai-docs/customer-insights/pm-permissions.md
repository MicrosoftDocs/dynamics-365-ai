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

The main administration page is the **Permissions** page where you can set up roles and permissions for using Customer 360 across your organization. 

 ![permissions.png](media/permissions.png)

In this screen you can view **organization members** for whom **roles** and **permissions** where assigned:
- Once you gave a permission to a specific user, this person's name will appear with a checked box next to it:
[]

- The **Type** column specifies whether it's a single member or a group
- A role is specified under the **Roles** column
- Lastly, you can sort the results by each of the columns by clicking on the arrow icon next to the column name:  
 
- **Adding Roles and Permissions** 
In terms of roles, it's possible to define organization members as either ***Administrators***, ***Contributors*** or ***Readers***. This definition process is done via the **Add Permissions** panel that can be accessed via  **Add** at the top of the permissions page:

 ![add-permissions.png](media/add-permissions.png)
 
Once the panel is opened, first you will need to find the person, group, or application to which you want to give the permission. Type a name in the **Name field** as shown below. As mentioned, beyond people, you can give permissions to applications that will connect to Customer 360 via our APIs.

[Permissions1]

Then, choose a role for that person/group/application as shown below:

 ![permissions-roles.png](media/permissions-roles.png)
 
 You can use the following table in order to know what options are available for each of the roles:

[permissins table]

- **Viewing current number of users per role:** This can be done via the **Roles** panel that can be accessed via **Roles** at the top of the permissions page:

(add permissions page with opened "roles" panel from the administration part on the app)

- **Filtering Permissions by a Role**: This can be achieved by opening the **Filter** panel through **Filter** at the top of the permissions page, and choosing whether to filter the permissions by the ***Administrator***, ***Contributor*** or ***Reader*** roles.

![permissions-filter.png](media/permissions-filter.png)
