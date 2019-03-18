---
title: "Customer Card add-in | MicrosoftDocs"
description: Customer Card add-in
ms.custom: ""
ms.date: 03/14/2019
ms.reviewer: ""
ms.service: dynamics-365-ai
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
---
# Customer Card add-in

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

## Requirements

- Dynamics 365 for Customer Engagement version 9.0 and later.
- Unified Interface enabled: Sales Hub, Customer Service Hub, Project Resource Hub. 
- Users who will use the Customer Insights Customer Card in Dynamics 365 for Customer Engagement need to be added as users on Dynamics 365 Customer Insights. You can do so in the **Permissions** page in the **Admin** section, as discussed later in this topic.

<!--note from editor: re sentence above--I'm not seeing where the reference is to the Permissions page   -->

> [!div class="mx-imgBorder"] 
> ![](media/permissions-page.png "Permissions page")

## Installation into Dynamics 365 for Customer Engagement

1. As an admin, go to the **Settings** section in Customer Engagement, and select **Solutions**. 

   > [!div class="mx-imgBorder"] 
   > ![](media/settings-solutions.png "Settings solutions")

2. Select the display name link for the Customer Insights solution.

   > [!div class="mx-imgBorder"] 
   > ![](media/select-display-name.png "Select display name")

3. Here you will configure the overall settings for the Customer Card add-in. The first step is to sign in with the admin Azure Active Directory (AAD) account you use to configure Customer Insights.

   > [!NOTE]
   > Check that the browser pop-up blocker is not blocking the authentication window when you select the **Authenticate** button. 

   > [!div class="mx-imgBorder"] 
   > ![](media/login-with-org-credentials.png "Log in with org credentials")

4. The next step is to select the Customer Insights instance you want to fetch data from.

   > [!div class="mx-imgBorder"] 
   > ![](media/select-instance-to-connect.png "Select instance to connect to")

5. The last step on the overall setting is to select which field in the Customer Insights Customer entity corresponds to the ID of the Contact entity in your Customer Engagement organization. 

   > [!div class="mx-imgBorder"] 
   > ![](media/contact-id-field.png "Contact id field")

6. Select **Save configuration** to save the setting. 

   > [!div class="mx-imgBorder"] 
   > ![](media/card-configuration-save.png "Save card configuration")

   > [!div class="mx-imgBorder"] 
   > ![](media/card-configuration-save2.png "Save card configuration")

7. Next, you will need to assign the following user roles:

   - Customer Insights Customizer: Assign this role to the users who will customize the content to be shown on the card for the whole organization.
   - Customer Insights Card Standard User: Assign this role to the users who will use the card for consumption, but who won’t customize. 
   
   > [!div class="mx-imgBorder"] 
   > ![](media/manage-user-roles.png "Manage user roles")

8. Now you can add the Customer Card controls into your contact form. To do so, go to the **Settings** section in Customer Engagement, and then select **Customizations**. 
 
   > [!div class="mx-imgBorder"] 
   > ![](media/settings-customizations.png "Settings Customizations")

9. Select **Customize the System**.

   > [!div class="mx-imgBorder"] 
   > ![](media/settings-customize-system.png "Settings Customize the System")

10.	Browse to the Contact entity, expand its menu, and then select **Forms**. 
    
    > [!div class="mx-imgBorder"] 
    > ![](media/contact-entity-definition.png "Contact entity definition")

11. Select the contact form to which you would like to add the Customer Card controls.

    > [!div class="mx-imgBorder"] 
    > ![](media/contact-active-forms.png "Contact active forms")

    > [!div class="mx-imgBorder"] 
    > ![](media/contact-form-designer.png "Contact form")

## Demographic control

1. To add the demographic control, in the form editor, drag any field from the field explorer to where you would like the demographic control to be placed.  

   > [!div class="mx-imgBorder"] 
   > ![](media/contact-form-designer2.png "Address 1: City field")

2. Select the field you just added, and select **Change Properties**. 

   > [!div class="mx-imgBorder"] 
   > ![](media/contact-form-designer3.png "Address 1: City field")

3. Clear the **Display label on the form** box. 
   
   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties.png "Field properties")

4. Go to the **Controls** tab and select **Add Control**.

   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control.png "Field properties add control")

5. Select **Demographic_Control**, and then select **Add**.

   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control-demographic.png "Field properties control demographic")

6. Select the **Web** option for **Demographic_Control**.

   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control-demographic2.png "Field properties control demographic")

7. Select **Save** and **Publish** to publish the contact form where you have placed the demographic control.

   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control-demographic3.png "Field properties publish control demographic")

8. Go to the published contact form. You will see the demographic control. You might need to sign in the first time you use it. To customize what you want to show on the demographic control, select the edit button in the upper-right corner. 

   The customization you perform here will apply across the organization.

   > [!div class="mx-imgBorder"] 
   > ![](media/demographic-control.png "Demographic control")

   > [!div class="mx-imgBorder"] 
   > ![](media/add-new-field.png "Add new field")

## Timeline control

1. In the form editor, drag any field from the field explorer to where you would like the demographic control to be placed.  

   > [!div class="mx-imgBorder"] 
   > ![](media/contact-form-designer4.png "Address 1: City field")

2. Select the field you just added, and then select **Change Properties**. 
 
   > [!div class="mx-imgBorder"] 
   > ![](media/contact-form-designer-publish.png "Address 1: City field publish")

3. Clear the **Display label on the form** box.
   
   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-display-label.png "Address 1: City field display label")

4. Go to the **Controls** tab, and select **Add Control**.

   
   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control2.png "Add control")


5. Select **Timeline_Control** and then **Add**.

   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control3.png "Add control")

6. Select the **Web** option for **Timeline_Control**.

   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-add-control4.png "Modify control properties")

7. Select **Save** and **Publish** to publish the contact form where you have placed the timeline control.
   
   > [!div class="mx-imgBorder"] 
   > ![](media/field-properties-publish-control.png "Publish form")

8. Go to the published contact form. You will see the timeline control. You might need to sign in the first time you use it. 

   > [!div class="mx-imgBorder"] 
   > ![](media/timeline-control.png "Timeline control")

