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

You can map to data from custom entities and fields by specifying Data mapping settings.

For more information on the entities used by Customer Service Insights, see [Dynamics 365 for Customer Service entities used by Customer Service Insights](customer-service-entities.md).

For more information on connecting to an environment, see [Use workspaces to connect to different customer service environments](use-workspaces.md).

## To specify mapping from custom entities and fields

1. Select the **Settings** button on the Customer Service Insights title bar and then select **Settings**.

   > ![Settings button](media/ai-csi-settings-button.PNG)

   AI for Customer Service Insights displays the Settings page.

2. Select **Data mapping** to display the Data mapping pane. If you have not created a workspace, Customer Service Insights prompts you to create one.

   > ![Data mapping pane](media/data-mapping-pane.PNG)

   For more information about creating a workspace, see [Use workspaces to connect to different customer service environments](use-workspaces.md).

3. If you are connected to a workspace, select the Incident destination entity to display the **Find your incident records** pane. Select the entities that contain your custom fields, and then select **Next**.

   > ![Find records pane](media/find-records-pane.PNG)

Here some things to keep in mind when you map your data to custom entities and fields:

* The drop-down list in the form only shows source fields in types that are compatible with the destination fields.

* Several fields require the Lookup attribute type in the Incident entity. These include Owning User, Owning Business Unit, Owning Team and Product. This fields carry information about which entity to look up and by which primary key value. They return the value of the primary field of the other entities.

* Several data fields in the Incident entity are pick lists, including Priority, Support Channel, SLA Status and Satisfaction. Picklist is an attribute type in Common Data Service that allows the selection of multiple options. Each option consists of a numeric value and a string label.

    For example, SLA Status indicates whether a case is compliant with the service-level agreement (SLA). You can define multiple different values for compliant cases. Customer Service Insights only uses the value 4 to identify noncompliant cases. The pick list values defined for Satisfaction indicates the customer satisfaction score (CSAT). Customer Service Insights reads value from 1 to 5 to calculate the average CSAT.