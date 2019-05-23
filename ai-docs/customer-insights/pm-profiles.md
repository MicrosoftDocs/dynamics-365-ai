---
title: "Customers | MicrosoftDocs"
description: 
ms.custom: ""
ms.date: 04/01/2019
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
# Customers

The **Customers** page presents a consolidated view of each customer based on profile data you gathered from all of your data sources. The page also lets you search for customers. Each customer profile is represented by a Customer Card tile as shown here:

> [!div class="mx-imgBorder"] 
> ![](media/profiles-customers.png "Customer profiles")

**Note:** If you get the following screen upon clicking the **Customers tab** on the app's left side menu, then it means that your administrator didn't define yet at least one searchable attribute using the **Search & Filter Index** screen:

> [!div class="mx-imgBorder"] 
> ![](media/add-attributes3.png "Add attributes")

If that is the case, your administrator can use the **Search & Filter Index** section to learn how to use the **Search & Filter Index** screen. Once at least one attribute was defined as searchable, you should get to the Customers page. 

Once gettng to the Customers page, you can start viewing your customers' profiles. You can always go to the next **Customers** page and view more customers profiles using the buttons in the lower-right corner of the page.

> [!div class="mx-imgBorder"] 
> ![](media/profiles-customers2.png "Customer profiles")


>[!NOTE]
> Customer profiles are available once you create the unified Customer entity. Make sure you complete the data unification process in order to unlock richer views of your customers. Visit the **Unify** section to learn more. 

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile.png "Customer Card tiles")

Select a customer tile to see additional information on that specific customer. As shown here, that information might include attributes, such as **Country**, **Email**, **Street address**, and **Phone**, that exist in one or more of your data sources:

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-customer-info.png "Customer Card tile customer info")

## Search for customers

Search for customers by entering an attribute name (for example, the customer’s name) in the search box. As an admin, you can always re-select and re-configure your searchable attributes using the **Search & filter index** screen that is accessible via the **Search & Filter Index** button:

> [!div class="mx-imgBorder"] 
> ![](media/search-filter-index.png "Search & filter index")

Note that the search will be executed only within the Customer Profile entity created during the data unification process.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-search.png "Customer Card tile search")

After selecting one of the customer tiles, you can also search for a specific attribute within this customer's information.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-search2.png "Customer Card tile search")

## Filter customers

Filtering customers can be done via a menu that includes your Customer Profile entity fields as filters. Same as for search, your admin will first need to define those fields as filterable using the **Search & filter index** screen. 

First, select **Filter**.

> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-filter.png "Customer Card tile filter")

Then, check the boxes next to the attributes you want to filter customers by. As with Search, you will be able to filter only by attributes that exist in your Customer Profile entity and that were defined by the administrator on the **Search & filter index** page.
Next to the filter panel you can see the number of customers that will result from your selected filters.

// replace 1
> [!div class="mx-imgBorder"] 
> ![](media/profiles-customers3.png "Customer profiles")

You can remove your saved filters using **Clear filters**.

// replace 2
> [!div class="mx-imgBorder"] 
> ![](media/customer-card-tile-clear-filter.png "Customer Card tile clear filter")

## Save filtered customer base as a segment

Once choosing at least one filter, you can choose to quickly produce a segment for all the customers that are included under your filter criteria. Click the **Save results as a segment**: 

// add 1

All you need to do is to select a segment type (see the **Segments** topic to learn more) as well as naming your segment. You might also choose to give it a **display name** (your segment will carry the display name in the Home page and Segments screen. It has no limitations while the **name** field does have some limitations). 

// add 2

If you wish to process your segment, in the next window choose **Activate**. If you wish to save the segment definition but activate it later choose the **Later** option.

// add 3
### Next Step
Review both the **Data Sources** and **Unify** sections, where you will learn to ingest and unify your data.
