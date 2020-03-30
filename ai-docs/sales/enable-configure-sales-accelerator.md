---
title: "Enable and configure the Sales accelerator in Dynamics 365 Sales Insights | MicrosoftDocs"
description: "Learn how to enable and configure the Sales accelerator in Dynamics 365 Sales Insights."
ms.date: 04/01/2020
ms.service: crm-online
ms.topic: article
author: udaykirang
ms.author: udag
manager: shujoshi
---

# Enable and configure the Sales accelerator

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

> [!IMPORTANT]
> - [!INCLUDE[cc_preview_features_definition](../includes/cc-preview-features-definition.md)]  
> - [!INCLUDE[cc_preview_features_expect_changes](../includes/cc-preview-features-expect-changes.md)]
> - Microsoft doesn't provide support for this preview feature. Microsoft Technical Support won’t be able to help you with issues or questions. Preview features aren't meant for production use and are subject to a separate [supplemental terms of use](https://go.microsoft.com/fwlink/p/?linkid=870960).

The Sales accelerator helps sellers in your organization increase their sales productivity and prioritize activities for the day through the work list available in Sales Hub app. A sales manager uses the sequence designer to create a sequence of activities&mdash;separated by time intervals&mdash;including emails, phone calls, and tasks. The sequence is then applied to leads or opportunities, and assigned to a seller automatically according to your organization's sales strategies.

As an administrator, you must enable and configure the Sales accelerator in your organization to make it available for sales managers and sellers to use. Follow these steps:

1. [Review the prerequisites and recommendation](#review-the-prerequisites-and-recommendations).

2. [Enable the preview](#enable-the-preview).

3. [Configure the Sales accelerator](#configure-the-sales-accelerator).

## Review the prerequisites and recommendations

### Prerequisites

Ensure that you meet the following requirements:

- Purchase a **Dynamics 365 Sales Insights** license, or start a trial to use advanced Sales Insights features.

- Enable advanced Sales Insights features. More information: [Enable and configure advanced Sales Insights features](intro-admin-guide-sales-insights.md#enable-and-configure-advanced-sales-insights-features)

### Recommendation

For the best experience of the Sales accelerator, enable and configure [predictive lead scoring](configure-predictive-lead-scoring.md) and [predictive opportunity scoring](configure-predictive-opportunity-scoring.md).

## Enable the preview

The Sales accelerator is available as a preview feature in Sales Insights. You must enable the preview and accept the preview terms and conditions to use the Sales accelerator in your organization.

1. Sign in to Dynamics 365 Sales Hub, and go to **Change area** > **Sales Insights settings**.

2. On the site map, under **Acceleration**, select **Sales accelerator (preview)**.

3. On the settings page, select **I agree to the preview terms and conditions** to enable the preview.

4. Select **Get started**.

    >[!div class="mx-imgBorder"]
    >![Enable preview](media/sa-enable-preview.png "Enable preview")

The Sales accelerator is now enabled, and you can configure it for your organization.

## Configure the Sales accelerator

1. Sign in to Dynamics 365 Sales Hub, and go to **Change area** > **Sales Insights settings**.

2. On the site map, under **Acceleration**, select **Sales accelerator (preview)**.

3. In the **Content and layout** section, select the **Lead** and **Opportunity** entities and their corresponding related forms, as required. The selected entity records will be displayed to sellers in the Sales Hub app, and sales managers will use the entities to configure the sequence that will be assigned to records to be displayed in the app. By default, the **Lead** and **Opportunity** entities are selected.

    >[!div class="mx-imgBorder"]
    >![Choose content and layout for entities](media/sa-choose-content-layout.png "Choose content and layout for entities") 

4. In the **Security roles** section, select one of the following options to provide permissions to users to access the Sales Hub app.

    >[!div class="mx-imgBorder"]
    >![Select security role](media/sa-select-security-role.png "Select security role") 
    
    | Security roles | Description |
    |----------------|-------------|
    | All security roles | Use this option to give access to view the Sales Hub app to all the security roles in your organization. |
    | Specific security roles | Use this option to specify security roles to give access to view the Sales Hub app to just a few users. Use the lookup box to add the security roles. |

5. Save and publish the configuration.

A confirmation message is displayed at the top of the page. Sales managers and sellers can now start using the Sales accelerator.

### See also

[Create and manage sequences](create-manage-sequences.md)  
[What is the Sales accelerator?](sales-accelerator-intro.md)