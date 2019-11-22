---
title: "Customer Card add-in | MicrosoftDocs"
description: Customer Card add-in
ms.custom: ""
ms.date: 11/22/2019
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
author: m-hartmann
ms.author: mhart
manager: shellyha
---
# Customer Card add-in

The Customer Card add-in gives you a 360-degree view of each of your customers. Once installed, you can start using  **Timeline Control** and **Demographic Control** to unlock rich insights on selected customers, including their location, age, latest activities, and more.

Note that a prerequisite to using the Customer Card is use of the **Search & Filter Index** screen (accessible via the **Customers** page) to index your data. Also note that:

- To view customer activities, they should first be defined using the **Activities** screen.
- To view customer KPIs, they should first be defined using the **Measures** screen.

## Requirements

- Model-driven apps in Dynamics 365 (such as Dynamics 365 Sales and Dynamics 365 Customer Service), version 9.0 and later.
- Unified Interface enabled: Sales Hub, Customer Service Hub, Project Resource Hub.
- Individuals who will use the Customer Card in model-driven Dynamics 365 apps need to be added as users. You can do so on the Customer Insights **Permissions** page in the **Admin** section, as discussed later in this topic.

  > [!div class="mx-imgBorder"]
  > ![Permissions page](media/permissions-page.png "Permissions page")

## Install Customer Card Add-in

1. As an admin, go to the **Settings** section in model-driven apps in Dynamics 365, and select **Solutions**.

   > [!div class="mx-imgBorder"]
   > ![Settings solutions](media/settings-solutions.png "Settings solutions")

2. Select the **Display Name** link for the Customer Insights solution.

   > [!div class="mx-imgBorder"]
   > ![Select display name](media/select-display-name.png "Select display name")

   If the Customer Insights solution does not appear in your list of solutions, select **Get Solutions from Marketplace** above the list. This will take you to Microsoft AppSource.

   > [!div class="mx-imgBorder"]
   > ![Get Solutions from Marketplace](media/get-solutions-from-marketplace2.png "Get Solutions from Marketplace")

   In Microsoft AppSource, search for the Dynamics Customer Card and select **Get It Now**. It may take some time for the solution to be installed to your environment.

3. Here you will configure the overall settings for the Customer Card add-in. Sign in with the admin Azure Active Directory (Azure AD) account you use to configure Customer Insights.

   > [!NOTE]
   > Check that the browser pop-up blocker does not block the authentication window when you select the **Authenticate** button.

   > [!div class="mx-imgBorder"]
   > ![Log in with org credentials](media/login-with-org-credentials.png "Log in with org credentials")

4. Select the Customer Insights instance you want to fetch data from.

   > [!div class="mx-imgBorder"]
   > ![Select instance to connect to](media/select-instance-to-connect.png "Select instance to connect to")

5. Select the field in the Customer Insights Customer entity that matches the ID of your Contact entity.

   > [!div class="mx-imgBorder"]
   > ![Contact ID field](media/contact-id-field.png "Contact ID field")

6. Select **Save configuration** to save the setting.

<!-- Is it sufficiently clear how to assign user roles? -->
7. Next, assign the following user roles:

   - **Customer Insights Card Customizer**: Assign this role to users who will customize the content shown on the card for the whole organization.
   - **Customer Insights Card Standard User**: Assign this role to users who will use the card for consumption, but who won’t customize.
  
8. Now you can add the Customer Card controls into your contact form. To do so, go to the **Settings** section in model-driven apps in Dynamics 365, and then select **Customizations**.

   > [!div class="mx-imgBorder"]
   > ![Settings customizations](media/settings-customizations.png "Settings customizations")

9. Select **Customize the System**.

10. Browse to the Contact entity, expand its menu, and then select **Forms**.

    > [!div class="mx-imgBorder"]
    > ![Expand Contact entity menu](media/contact-entity-definition.png "Expand Contact entity menu")

11. Select the contact form to which you would like to add the Customer Card controls.

    > [!div class="mx-imgBorder"]
    > ![Select Contact form](media/contact-active-forms.png "Select Contact form")

    > [!div class="mx-imgBorder"]
    > ![Contact form summary](media/contact-form-designer.png "Contact form summary")

## Demographic control

1. To add the demographic control, in the form editor, drag any field from the Field Explorer to where you would like the demographic control to be placed.

   > [!div class="mx-imgBorder"]
   > ![Choose a field in Field Explorer](media/contact-form-designer2.png "Choose a field in Field Explorer")

2. Select the field you just added, and select **Change Properties**.

   > [!div class="mx-imgBorder"]
   > ![Select Change Properties](media/contact-form-designer3.png "Select Change Properties")

3. Clear the **Display label on the form** check box.

   > [!div class="mx-imgBorder"]
   > ![Clear the check box](media/field-properties.png "Clear the check box")

4. Go to the **Controls** tab and select **Add Control**.

5. Select **Demographic_Control**, and then select **Add**.

6. Select the **Web** option for **Demographic_Control**.

   > [!div class="mx-imgBorder"]
   > ![Select the Web option](media/field-properties-add-control-demographic2.png "Select the Web options")

7. Select **Save** and **Publish** to publish the contact form where you have placed the demographic control.

   > [!div class="mx-imgBorder"]
   > ![Save and then publish](media/field-properties-add-control-demographic3.png "Save and then publish")

8. Go to the published contact form. You will see the demographic control. You might need to sign in the first time you use it.

   To customize what you want to show on the demographic control, select the edit button in the upper-right corner. This customization will apply across the organization.
  
   > [!div class="mx-imgBorder"]
   > ![Demographic control](media/demographic-control.png "Demographic control")

   > [!div class="mx-imgBorder"]
   > ![Add new field](media/add-new-field.png "Add new field")

## Timeline control

1. In the form editor, drag any field from the Field Explorer to where you would like the demographic control to be placed.  

   > [!div class="mx-imgBorder"]
   > ![Select field in Field Explorer](media/contact-form-designer4.png "Select field in Field Explorer")

2. Select the field you just added, and then select **Change Properties**.

   > [!div class="mx-imgBorder"]
   > ![Select Change Properties](media/contact-form-designer-publish.png "Select Change Properties")

3. Clear the **Display label on the form** check box.
  
   > [!div class="mx-imgBorder"]
   > ![Clear check box](media/field-properties-display-label.png "Clear check box")

4. Go to the **Controls** tab, and select **Add Control**.

5. Select **Timeline_Control** and then **Add**.

6. Select the **Web** option for **Timeline_Control**.

   > [!div class="mx-imgBorder"]
   > ![Select Web option](media/field-properties-add-control4.png "Select Web option")

7. Select **Save** and **Publish** to publish the contact form where you have placed the timeline control.
  
   > [!div class="mx-imgBorder"]
   > ![Publish form](media/field-properties-publish-control.png "Publish form")

8. Go to the published contact form. You will see the timeline control. You might need to sign in the first time you use it.

   > [!div class="mx-imgBorder"]
   > ![Timeline control](media/timeline-control.png "Timeline control")
