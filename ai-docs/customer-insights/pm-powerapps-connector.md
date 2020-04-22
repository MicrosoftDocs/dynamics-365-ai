---
title: "Power Apps connector | Microsoft Docs"
description: "Connect Dynamics 365 Customer Insights with Power Apps and Power Automate."
ms.date: 04/22/2020
ms.reviewer: nikeller
ms.service: dynamics-365-ai
ms.topic: "get-started-article"
author: m-hartmann
ms.author: mhart
manager: shellyha
---

# Microsoft Power Apps connector (preview)

Bring unified customer profiles into your personalized apps with Power Apps.

## Connect Power Apps to Customer Insights

Customer Insights is one of the many [available sources for data in Power Apps](https://docs.microsoft.com/powerapps/maker/canvas-apps/working-with-data-sources).

Refer to the Power Apps documentation to learn how to [add a data connection to an app](https://docs.microsoft.com/powerapps/maker/canvas-apps/add-data-connection).

## Available entities

After adding Customer Insights as a data connection, you can choose the following entities in Power Apps:

- Customer: to use data from the [unified customer profile](pm-profiles.md).
- Unified Customer Activity: to display the [activity timeline](pm-activities.md) on the app.

## Example gallery control

An example to use Customer Insights data, is to show customer profiles in a [gallery control](https://docs.microsoft.com/powerapps/maker/canvas-apps/add-gallery).

1. Add a **Gallery** control to an app you're building.

> [!div class="mx-imgBorder"]
> ![Add a gallery element](media/connector-powerapps9.png "Add a gallery element")

1. Select **Customer** as the data source for items.

    > [!div class="mx-imgBorder"]
    > ![Select a data source](media/choose-data-source-powerapps.png "Select a data source")

1. You can change the data panel on the right to select which field for the Customer entity to show on the gallery.

1. If you want to show any field from the selected customer on the gallery, fill in the Text property of a label:  **{Name_of_the_gallery}.Selected.{property_name}**

    Example: Gallery1.Selected.address1_city

1. To display the unified timeline for a customer, add a Gallery element, and add the Items property: **Filter('Unified Customer Activity', CustomerId = {Customer_Id})**

    Example: Filter('Unified Customer Activity', CustomerId = Gallery1.Selected.CustomerId)
