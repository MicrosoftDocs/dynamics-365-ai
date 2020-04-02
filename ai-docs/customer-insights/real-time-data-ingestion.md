---
title: "Real-time data ingestion for Dynamics 365 Customer Insights | Microsoft Docs"
description: "General information about real-time capabilities in Customer Insights."
ms.date: 04/02/2020
ms.reviewer: mhart
ms.service: dynamics-365-ai
ms.topic: "article"
author: adasatu
ms.author: a-dasatu
manager: shellyha
---

# Real-time data ingestion

The near real-time functionality lets you see the latest interactions that your customers have made with your products or services.

## Real-time creation of activities

The real-time feature can be implemented by building your own pipeline and connect directly to the Customer Insights real-time API.

This service lets you publish a new [activity](pm-activities.md) from your source system (an *individual* source record) to a [unified customer profile](pm-profiles.md) in Customer Insights, within *seconds*. They are referred to as *real-time updates*.

On the other hand, the refreshes in Customer Insights include a *large number* of records. They are processed in bulk and take *much longer*. Those are referred to as *scheduled refreshes*.

This distinction is important. Real-time updates are not a replacement for scheduled refreshes.

For example, activities ingested through the real-time API will only be kept for 30 days. If you want them to be included in Customer Insights for longer you should ensure that they also get added to the data source, so that they get ported during the next scheduled batch update of Customer Insights.

Following the same logic, activities added only through the real-time API are not part of exports and won't show up in PowerBI either.

> [!NOTE]
>
> - Activities don't change once created. They are only deleted when the profile is deleted.
> - Currently, the unified profile and the customer card, including segments and enrichments, won't update based on the new activity.

## Connect directly to the real-time API

Details of this API, including parameters and responses, can be found in the **RealTime** section on the [Swagger UI page](https://global.api.ci.ai.dynamics.com/swagger/index.html). [Learn more about how to use the Customer Insights Swagger webpage](pm-apis.md#how-to-use-the-customer-insights-swagger-webpage).

### Example of a call to the real-time API

Prerequisites: have an instance with activities (only activities set up in the **activities screen** can be received by Customer Insights in real-time). To add an activity, an entity with date/time type fields is required.

1. Go to the [Swagger UI page](https://global.api.ci.ai.dynamics.com/swagger/index.html).

2. On that page, go to the **EntityData** section and select **POST** /api/instances/{instanceId}/data/{entityName}.

3. Select **Try it out**.

3. In the field **instanceId**, enter your instance ID which you find in the URL of your Cusomter Insights instance, or in **Settings** > **Environments**.

4. Under relative path, enter the name of the entity you chose, following this format: **DataSource_EntityName**.    
To find the entity name format, go to **Data** > **Entities** and select the entity you want to use.

   > [!div class="mx-imgBorder"]
   > ![Entity name format](media/real-time-entity.png "Entity name format")

5. Under entity (request body) enter the new activity as a json object. The format of the entity in the request body is the same as the one received when performing a GET call on this resource.

   All the fields of the json object sent in the request body can be seen in the **Fields** tab on the selected entity in **Data** > **Entities**.
