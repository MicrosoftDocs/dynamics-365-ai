---
title: "Real-time data ingestion for Dynamics 365 Customer Insights | Microsoft Docs"
description: "General information about real-time capabilities in Customer Insights"
ms.date: 05/01/2020
ms.reviewer: mhart
ms.service: dynamics-365-ai
ms.topic: "article"
author: adasatu
ms.author: a-dasatu
manager: shellyha
---

# Real-time data ingestion (preview)

The near real-time functionality lets you see, within seconds, the latest interactions that your customers have made with your products or services.

In Customer Insights, scheduled refreshes include large numbers of records and several complex operations. First, data is pulled from the data source into Customer Insights. Next, the data is unified, and then enriched with additional information. Every run of this process can take minutes to hours.

The real-time functionality provides data immediately for consumption in Customer Insights, until the subsequent scheduled refresh pulls this data from the data source.

Real-time updates have an expiration time after which they no longer override the value from the data source:
- Profile updates will only be kept for 4 hours
- Activities will only be kept for 30 days

Those default values are API call parameters that you can change. Their aim is to ensure that your source data remain your source of truth. Therefore, if you want real-time updates to be included in Customer Insights for longer, you need to ensure that they also get added into your data source, so they get pulled during the next scheduled refresh of Customer Insights.

## Real-time update of the unified customer profile fields

Updated profiles will show in the customer card view, or any other visualization of Customer Insights data, within a few seconds.

Since for the moment real time operations first take place after the data unification has happened, they only apply to the unified customer profiles. Consequently, real time profile changes will not update measures, segment membership or enrichments.

**Limitations**
-	Customer profiles can be updated, but not created or deleted.
-	Exporting real-time updates to external systems, like **Power BI**, is not possible at the moment.


## Real-time creation of activities

The real-time API lets you publish a new activity from your source system (an individual source record) to a unified customer profile in Customer Insights. The new activity will be available as a unified activity in that unified customer profile's timeline within seconds. You can see the timeline in the customer card view in Customer Insights or any other timeline integration you configured.

> [!NOTE]
>
> - Activities are immutable. They don't change once created.
> - Currently, segments and measures won't update based on the new activity.
> - Activities added only through the real-time API are not part of exports and won't show up in PowerBI.

We will now present you two ways to connect to the Customer Insights real-time API:
- indirectly, via a “plug and play” [Dynamics 365 Customer Insights connector] (https://docs.microsoft.com/en-us/connectors/customerinsights/)
- directly, with code

Both ways share the following **prerequisites**:
- A Customer Insights instance
- Unified customer profiles
- Activities configured and run
- Contributor or Administrator level permissions (for authenticating your account)


## Connect via the Dynamics 365 Customer Insights connector

The real-time API can ingest data from a dedicated Power Platform Connector, the  [Dynamics 365 Customer Insights connector] (https://docs.microsoft.com/en-us/connectors/customerinsights/), without the need to write and deploy any code.
The connector can do the same real-time actions as the API. Please note that you will need a valid license for premium connectors (details about licensing can be found in the [Power Apps and Power Automate licensing FAQs] (https://docs.microsoft.com/en-us/power-platform/admin/powerapps-flow-licensing-faq)).
Read more about how to use the  [Dynamics 365 Customer Insights connector] (https://docs.microsoft.com/en-us/connectors/customerinsights/) in the following documentation:
-	in Power Platform’s [Power Apps and/or Power Automate] (https://docs.microsoft.com/en-us/connectors/)
-	in Azure [Logic Apps] (https://docs.microsoft.com/en-us/azure/connectors/apis-list) (some coding required)

For details about the creation of flows please refer to the [Power Automate documentation] (https://docs.microsoft.com/en-us/power-automate/).



## Connect directly to the real-time API

The real-time feature can also be used by building your own pipeline and connecting directly to the Customer Insights real-time API.
Please note that you can post an activity in the format of your source system or in the UnifiedActivity format (get it by making an an API call to /api/instances/{instanceId}/manage/entities/UnifiedActivity).

Details of this API, including parameters and responses, can be found in the **EntityData** section on the [Swagger UI page](https://global.api.ci.ai.dynamics.com/swagger/index.html). [Learn more about how to use the Customer Insights Swagger webpage](pm-apis.md#how-to-use-the-customer-insights-swagger-webpage).
