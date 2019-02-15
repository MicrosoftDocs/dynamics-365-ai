---
title: "Customer Card add-in | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 11/05/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Customer Card add-in

### Requirements

- Dynamics 365 for Customer Engagement v9.0+ 
- Unified Interface enabled: Sales Hub, Customer Service Hub, Project Resource Hub 
- Users will use the Customer Insights Customer Card in Customer Engagement need to be added as users on Customer Insights. You can do so in the **Permissions** page in the **Admin** section. See below.

> [!div class="mx-imgBorder"] 
> ![](media/permissions-page.png "Permissions page")

### Installation into Dynamics 365 for Customer Engagement

1. As an admin, go to the **Settings** section in Dynamics 365, and select **Solutions**. 

   > [!div class="mx-imgBorder"] 
   > ![](media/settings-solutions.png "Settings solutions")

2. Select the display name link for the Customer Insights solution.

   > [!div class="mx-imgBorder"] 
   > ![](media/select-display-name.png "Select display name")

3. Here you will configure the overall settings for the customer card add-in. First step is log in with an admin Azure Active Directory (AAD) account you use to configure Customer Insights.

   > [!NOTE]
   > Check that the browser pop-up blocker is not blocking the authentication window when you click on the authenticate button. 

   > [!div class="mx-imgBorder"] 
   > ![](media/login-with-org-credentials.png "Log in with org credentials")

4. Next step is to select the Customer Insights instance you wish to fetch data from.

   > [!div class="mx-imgBorder"] 
   > ![](media/select-instance-to-connect.png "Select instance to connect to")

5. Last step on the overall setting is to select which field on the Customer Insights Customer entity corresponds to the id of the Contact entity on your Dynamics 365 organization. 

   > [!div class="mx-imgBorder"] 
   > ![](media/contact-id-field.png "Contact id field")

6. Click Save configuration to persist the setting. 

   > [!div class="mx-imgBorder"] 
   > ![](media/card-configuration-save.png "Save card configuration")

   > [!div class="mx-imgBorder"] 
   > ![](media/card-configuration-save2.png "Save card configuration")

7. Next you will need to assign the following user roles:

   - Customer Insights Customizer: Assign this role to the users who will customize the content to be shown on the card for the whole organization.
   - Customer Insights Card Standard User: Assign this role to the users who will use the card for consumption, but who won’t customize. 
   
   > [!div class="mx-imgBorder"] 
   > ![](media/manage-user-roles.png "Manage user roles")

8. Now you can add the Customer Card controls into your Contact form. To do so, go to the Settings section in Dynamics 365, and click on Customizations. 
 
   > [!div class="mx-imgBorder"] 
   > ![](media/settings-customizations.png "Settings Customizations")

9. Click on Customize the System.

   > [!div class="mx-imgBorder"] 
   > ![](media/settings-customize-system.png "Settings Customize the System")

10.	Browse to the Contact entity, expand its menu and click on Forms. 
    
    > [!div class="mx-imgBorder"] 
    > ![](media/contact-entity-definition.png "Contact entity definition")

11. Select the contact form you would like to add the customer card controls.

    > [!div class="mx-imgBorder"] 
    > ![](media/contact-active-forms.png "Contact active forms")












### Demographic control


### Timeline control


