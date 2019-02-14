---
title: "Map your data to custom entities and fields"
description: "Learn how to generate insights by mapping your data to custom data entities and fields​."
keywords: ""
ms\.date: 2/8/2019
ms.service:
  - "dynamics-365-ai"
ms.topic: article
ms.assetid: 
author: stevesaunders1952
ms.author: stevesaunders1952
manager: shellyha
---

# Map your data to custom entities and fields

Dynamics 365 Customer Service Insights works by default with Dynamics 365 Customer Service data. The built-in dashboards and interactive charts in Customer Service Insights use data stored in default Dynamics 365 entities and data fields, primarily in the Incident (case) entity and several other related entities in Common Data Service.

However, you may want to generate insights by mapping to data from custom entities and fields in Common Data Services (CDS). Mapping to data from custom entities and fields in Common Data Services can be useful in the following cases:

* You are not a Dynamics 365 for Customer Service customer.
* You are a Dynamics 365 for Customer Service customer, but your service solution is customized and you use custom CDS entities and fields to store support case data.
* You want to use a custom field other than the support case title in your Dynamics 365 Customer Service Insights dashboards.

When you create a Customer Service Insights workspace and connect to a Dynamics 365 environment, Customer Service Insights prompts you to map your data:

* If the environment doesn't have an Incident entity.
* If the environment has an Incident entity but it doesn’t contain enough required data.

After a workspace is created, you can map to data from custom entities and fields by specifying Data mapping settings.

For more information on the entities used by Customer Service Insights, see [Dynamics 365 for Customer Service entities used by Customer Service Insights](customer-service-entities.md).

For more information on creating a workspace and connecting to an environment, see [Use workspaces to connect to different customer service environments](use-workspaces.md).

## To map data when you connect to a Dynamics 365 environment

1. Follow the steps in [Use workspaces to connect to different customer service environments](use-workspaces.md) to connect to a Dynamics 365 environment.

2. If the environment doesn't have an Incident entity or if the environment has an Incident entity but it doesn’t contain enough required data, Customer Service Insights displays the **Map your data** screen. Click **Get started** to begin mapping your data.

   > ![Map your data](media/map-your-data.png)

3. On the **Find your incident records** page, select the entity or entities that contain the data fields you want to use for mapping, and then click **Next**.

   > ![Select entity](media/select-entity.png)

4. On the **Map your incident records** page, select the data fields you want to use from the drop-down menu. Some fields have been mapped automatically. Then click **Done**.

   > ![Map fields](media/map-fields.png)

## To map data by specifying Data mapping settings

1. Select the **Settings** button on the Customer Service Insights title bar and then select **Settings**.

   > ![Settings button](media/ai-csi-settings-button.png)

   Customer Service Insights displays the **Settings** page.

2. Select **Data mapping** to display the Data mapping pane. Customer Service Insights displays the available destination entities.

   > ![Data mapping pane](media/data-mapping-pane.png)

3. To edit your mapping settings for an entity, hover over the entity in the list and click the edit icon.

   > ![Edit entity](media/edit-entity.png)

    Customer Service Insights displays the **Map your incident records** page, where you can update the data mapping for the entity.

4. You can view the status of the mapping in the **Mapped Fields** column.

   > ![View mapping](media/view-mapping.png)

Here some things to keep in mind when you map your data to custom entities and fields:

* The drop-down list in the form only shows source fields in types that are compatible with the destination fields.

* Several fields require the Lookup attribute type in the Incident entity. These include Owning User, Owning Business Unit, Owning Team and Product. This fields carry information about which entity to look up and by which primary key value. They return the value of the primary field of the other entities.

* Several data fields in the Incident entity are pick lists, including Priority, Support Channel, SLA Status and Satisfaction. Picklist is an attribute type in Common Data Service that allows the selection of multiple options. Each option consists of a numeric value and a string label.

    For example, SLA Status indicates whether a case is compliant with the service-level agreement (SLA). You can define multiple different values for compliant cases. Customer Service Insights only uses the value 4 to identify noncompliant cases. The pick list values defined for Satisfaction indicates the customer satisfaction score (CSAT). Customer Service Insights reads value from 1 to 5 to calculate the average CSAT.