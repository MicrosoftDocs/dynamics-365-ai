---
title: "Customer Card add-in | Microsoft Docs"
description: "Install and configure the Customer Card add-in for Dynamics 365 Customer Insights."
ms.date: 02/03/2020
ms.reviewer: ""
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Customer Card add-in

The Customer Card add-in gives you a 360-degree view of each of your customers. Once installed, you can start using  **Timeline Control** and **Demographic Control** to unlock rich insights on selected customers, including their location, age, latest activities, and more.

A prerequisite to using the Customer Card is use of the **Search & Filter Index** screen (accessible via the **Customers** page) to index your data. Also note that:

- To view customer activities, they should first be defined using the **Activities** screen.
- To view customer KPIs, they should first be defined using the **Measures** screen.

## Requirements

- Model-driven apps in Dynamics 365 (such as Dynamics 365 Sales and Dynamics 365 Customer Service), version 9.0 and later.
- Unified Interface enabled: Sales Hub, Customer Service Hub, Project Resource Hub.
- Individuals who will use the Customer Card in model-driven Dynamics 365 apps need to be added as users. You can do so on the Customer Insights **Permissions** page in the **Admin** section, as discussed later in this topic.

## Install the Customer Card Add-in

1. As an admin, go to the **Settings** section in model-driven apps in Dynamics 365, and select **Solutions**.

2. Select the **Display Name** link for the Customer Insights solution.

   > [!div class="mx-imgBorder"]
   > ![Select display name](media/select-display-name.png "Select display name")

   If the Customer Insights solution doesn't appear in your list of solutions, select **Get Solutions from Marketplace** above the list. This will take you to Microsoft AppSource.

   In Microsoft AppSource, search for the Dynamics Customer Card and select **Get It Now**. It may take some time for the solution to be installed to your environment.

3. Here you'll configure the overall settings for the Customer Card add-in. Sign in with the admin Azure Active Directory (Azure AD) account you use to configure Customer Insights.

   > [!NOTE]
   > Check that the browser pop-up blocker does not block the authentication window when you select the **Authenticate** button.

<!-- we need to check that we use the right UI text for "Authenticate"-->

4. Select the Customer Insights instance you want to fetch data from.

5. Select the field in the Customer Insights Customer entity that matches the ID of your Contact entity.

   > [!div class="mx-imgBorder"]
   > ![Contact ID field](media/contact-id-field.png "Contact ID field")

6. Select **Save configuration** to save the setting.

<!-- Is it sufficiently clear how to assign user roles? -->
7. Next, assign the following user roles:

   - **Customer Insights Card Customizer**: Assign this role to users who will customize the content shown on the card for the whole organization.
   - **Customer Insights Card Standard User**: Assign this role to users who will use the card for consumption, but who won’t customize.
  
8. Now you can add the Customer Card controls into your contact form. To do so, go to the **Settings** section in model-driven apps in Dynamics 365, and then select **Customizations**.
  
    To associate an Account form to an organization, you can select the Customers Insights Customer entity that corresponds to the organization ID (CompanyId in this case).
   > [!div class="mx-imgBorder"]
   > ![Contact ID field](media/customer-card-add-in-b2b.png "Account ID field")

9. Select **Save configuration** to save the settings.

   > [!div class="mx-imgBorder"]
   > ![Settings customizations](media/settings-customizations.png "Settings customizations")

10. Select **Customize the System**.

11. Browse to the Contact entity, expand its menu, and then select **Forms**.

    > [!div class="mx-imgBorder"]
    > ![Expand Contact entity menu](media/contact-entity-definition.png "Expand Contact entity menu")

12. Select the contact form to which you would like to add the Customer Card controls.

    > [!div class="mx-imgBorder"]
    > ![Select Contact form](media/contact-active-forms.png "Select Contact form")

## Demographic control

1. To add the demographic control, in the form editor, drag any field from the Field Explorer to where you would like the demographic control to be placed.

   > [!div class="mx-imgBorder"]
   > ![Choose a field in Field Explorer](media/contact-form-designer2.png "Choose a field in Field Explorer")

2. Select the field you just added, and select **Change Properties**.

3. In the **Field Properties** dialog, clear the **Display label on the form** check box.

4. Go to the **Controls** tab and select **Add Control**.

5. Select **Demographic_Control**, and then select **Add**.

6. Select the **Web** option for **Demographic_Control**.

   > [!div class="mx-imgBorder"]
   > ![Select the Web option](media/field-properties-add-control-demographic2.png "Select the Web options")

7. Select **Save** and **Publish** to publish the contact form where you've placed the demographic control.

8. Go to the published contact form. You'll see the demographic control. You might need to sign in the first time you use it.

   To customize what you want to show on the demographic control, select the edit button in the upper-right corner. This customization will apply across the organization.
  
   > [!div class="mx-imgBorder"]
   > ![Demographic control](media/demographic-control.png "Demographic control")

## Timeline control

1. In the form editor, drag any field from the Field Explorer to where you'd like to place the demographic control.  

2. Select the field you just added, and then select **Change Properties**.

3. In the **Field Properties** dialog, clear the **Display label on the form** check box.

4. Go to the **Controls** tab, and select **Add Control**.

5. Select **Timeline_Control** and then **Add**.

6. Select the **Web** option for **Timeline_Control**.

   > [!div class="mx-imgBorder"]
   > ![Select Web option](media/field-properties-add-control4.png "Select Web option")

7. Select **Save** and **Publish** to publish the contact form where you've placed the timeline control.

8. Go to the published contact form. You'll see the timeline control. You might need to sign in the first time you use it.
