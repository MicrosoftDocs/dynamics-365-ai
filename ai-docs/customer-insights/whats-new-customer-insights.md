---
title: "New and upcoming features (Dynamics 365 Customer Insights) | Microsoft Docs"
description: "Information about new features, improvements, and bug fixes in Dynamics 365 Customer Insights releases."
ms.date: 07/07/2020
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
ms.reviewer: midevane
manager: shellyha
---

# What's new in Dynamics 365 Customer Insights

We're excited to announce our newest updates! This article summarizes public preview features, general availability enhancements, and feature updates. To see the long-term feature plans, take a look at the [Dynamics 365 and Power Platform release plans](https://docs.microsoft.com/dynamics365/release-plans/).

You can also watch the following video to learn more about the capabilities planned for 2020 release wave 1. 

> [!VIDEO https://www.youtube.com/embed/jQh-7pscH30]

We roll out updates on a region-by-region basis. So certain regions might see features before others. Unless specified differently, you don't need to take any action and we'll update the app automatically with no downtime.

> [!TIP]
> To submit and vote on feature requests and product suggestions, go to the [Dynamics 365 Application Ideas portal](https://experience.dynamics.com/ideas/categories/?forum=79a8c474-4e35-e911-a971-000d3a4f3343&forumName=Dynamics%20365%20Customer%20Insights).

## June 2020 updates

The Dynamics 365 Customer Insights updates in June 2020 includes several features, performance upgrades, and bug fixes.

### New and updated features in June 2020

#### Enrichment

- **Enrichment with company data from Leadspace**
  
  Define fields in unified customer profiles that are used to look up related company data from Leadspace. After running the enrichment process, B2B profiles are enriched with additional attributes including company size, location, industry, and more.    
  This collaboration allows you to improve the quality of your data with input from third-party services. To use this enrichment you'll need a license from Leadspace to access its B2B company data. Customer Insights will use that license to keep your data enriched continuously.    
  For more information, see [Enrichment of company profiles with Leadspace](enrichment-leadspace.md).

- **Enrichment hub page**

  All available data enrichment from first- and third-party enrichment providers gets configured in the same place. Configuring data enrichment is a seamless experience that is managed from a common place.    
  For more information, see [Enrichment for customer profiles](enrichment-hub.md).

- **Separate brand and interest affinity enrichment**

  The brands and interests affinities are now available as two independent enrichments. This gives you the flexibility to configure and manage them separately, depending on your business requirements or needs.    
  For more information, see [Enrich customer profiles with brand and interest affinities](enrichment-microsoft-graph.md).

#### Extensibility

- **Clickable URLs for unified activities on the Dynamics 365 Customer Card Add-in**

  The unified activities in the Customer Card Add-in are now showing clickable URLs if such URLs have been defined in Customer Insights during the configuration of activities.    
  For more information, see [Customer Card Add-in](customer-card-add-in.md).

- **Brand and interest affinities available on the Dynamics 365 Customer Card Add-in**

  A new control on the Dynamics 365 Customer Card Add-in lets you show brand and interest enrichments on your contacts on model-driven Dynamics 365 apps.    
  For more information, see [Customer Card Add-in](customer-card-add-in.md).

- **Additional Power Automate triggers**

  We have extended our triggers for Power Automate and added the following triggers:
  - Get a notification or perform an action when an automated full refresh (data sources, unification, segments, measures, exports) completes
  - Define a threshold for a business measure. For example, you can create a notification that gets sent when the defined threshold is passed. Additionally, the trigger brings information that allows you to build more complex workflows in Power Automate.    
  For more information, see [Power Automate connector](export-power-automate.md)

- **Export to Facebook Ads Manager**
  
  This capability lets you export segments from Customer Insights to Facebook Ads Manager. Segments are exported as custom audiences to use unified customer profiles from Customer Insights in Facebook marketing campaigns and ads. The custom audiences are also usable to create campaigns on Instagram through Facebook Ads Manager.    
  For more information, see [Connector for Facebook Ads Manager](export-facebook.md).

#### Predictions

- **Subscription churn prediction**

Follow a simple, guided experience to create churn prediction in subscription areas like cloud services, customer membership, and other sectors. 

The subscription churn prediction feature enables you to predict the likelihood of a customer stopping the use of subscription-based products or services without engaging a data scientist. Using the prediction score, you can combine other information about your customers to create segments of high churn risk.  With the help of this segment, you can use integrations with Customer Insights to directly target customers in marketing, customer support, and other scenarios to reduce the risk of churn for specific customers to improve revenue and reduce cost.

Within the experience, you can configure the definition of churn as a time-based window specific to your business.  For example, a video streaming business that has a monthly subscription process might want to consider a customer to have churned after 15 days after the expiration of their subscription.

As you continue through the prediction, we'll guide you through what data is needed, and enable you to map data about your business to fields required to predict churn for your customers. As business information changes, you can also set a schedule to retrain on new information in your system to adapt to changing business circumstances.

For more information, see [Subscription churn prediction (preview)](predict-subscription-churn.md).

#### Segments

#### System administration



## May 2020 updates

The Dynamics 365 Customer Insights updates in May 2020 includes several features, performance upgrades, and bug fixes.

### New and updated features in May 2020

#### Data ingestion

- **Real-time data ingestion: history views**

  When using our API to ingest real-time updates, you can see up to 30 days of aggregated history for these updates. You have access to aggregates of all successful or failed API calls including their outcome, source system, and other useful metadata.    
  For more information, see [Real-time data ingestion](real-time-data-ingestion.md).

- **Real-time data ingestion: profile updates**

  This extension of the real-time data ingestion lets you see, within seconds, changes to specific user profile fields.    
  In addition to the real-time functionality for activities, Customer Insights supports low latency updates to profile fields. Real-time updates for profile fields have an expiration time and are therefore not a replacement for scheduled refreshes.    
  For more information, see [Real-time data ingestion](real-time-data-ingestion.md).

#### Extensibility

- **Updated timeline and pagination on the Customer Card Add-in**

  The timeline of the Customer Card Add-in solution for Dynamics 365 model-driven apps matches the activity timeline in Customer Insights. The pagination of the timeline improved, showing up to 50 activities at once. It also allows loading additional activities in the timeline.    
  For more information, see [Customer Card Add-in](customer-card-add-in.md).

- **Power Automate trigger for segment changes**

  Triggers for Power Automate define what you can build a flow from. The newly added trigger lets you define a threshold for a segment. For example, you can create a notification that gets sent when the defined threshold is passed.    
  For more information, see [Power Automate connector](export-power-automate.md).

- **Multitenant support for custom models**

  Configure workflows for custom models with a web service of a different Azure Machine Learning tenant. You can sign in to the Azure Machine Learning tenant from Customer Insights when creating a new workflow for custom models. This capability is an addition to the existing capability of integrating with your own custom Azure Machine Learning web service.    
  For more information, see [Custom machine learning models](custom-models.md).

#### Segments

- **Entity path automation**

  When creating a segment in Customer Insights, users need to define the entity path. This capability takes a first step at automating the entity path definition so you can focus on the segmentation criteria that you have in mind.    
  If the entity by which you want to segment your customers is directly related to the unified customer entity, you won't need to define the entity path anymore. However, if there is more than one possible entity path, you still need to define it manually.

- **Actions on multiple segments**
  
  Users can select multiple segments and take actions on them, like refreshing the segments, with a single click.    

- **Refresh segments**

  Users can refresh a single segment or select only the segments they want to refresh.    

  
- **Improvements to compounded segments**

  Users can create, edit, and delete segments that are based on other segments. For example, a segment constructed on another segment that was constructed on a third segment.    

- **Segment list page**

  The new design of the segments page uses a list format that lets you see more segments at once. A search field is added to find segments quickly. Users can now apply actions like downloading or deleting on multiple segments at once. A new trend experience is introduced to quickly identify significant changes on segments.    
  For more information, see [Create and manage segments](segments.md).

#### System administration

- **Customer Insights available in Microsoft Dynamics 365 Online Government**

  With more and more channels for interactions, citizen data is scattered across myriad systems, leading to siloed data, and a fragmented view of information about citizen interactions. Without a complete view of each citizen's interactions across channels, it's impossible for governments to modernize at scale. Microsoft is committed to supporting the technology needs of government to keep up with citizen expectations for consistent and responsive experiences.    
  With 2020 release wave 1, Dynamics 365 Customer Insights will be available for the Government Community Cloud (GCC), an environment built to meet the higher compliance needs of United States government agencies. Agencies gain a unified view of citizens and use prebuilt AI to derive insights that improve interactions, empower employees, and transform communities, while reducing IT complexity and meeting United States compliance and security standards. Dynamics 365 Government meets the demanding requirements of the US Federal Risk and Authorization Management Program (FedRAMP), enabling United States federal agencies to benefit from the cost savings and rigorous security of the Microsoft Cloud.

## April 2020 updates

The Dynamics 365 Customer Insights updates in April 2020 includes several features, performance upgrades, and bug fixes.

### New and updated features in April 2020

#### Activities

- **Map activity entity to standard activity type**
  
  Activity configuration and storage are currently based on a static design to view them in a timeline. The semantic meaning of activities, which has potential for multiple use-cases in AI models, isn't fully used at the moment. We plan to make the activity timeline more dynamic, based on the activity type and better semantic understanding of the activities. This feature aims to identify the activity type as defined in Common Data Model for any ingested activity.
  For more information, see [Customer activities](activities.md).

#### Data ingestion

- **Real-time data ingestion: activities**
  
  Real-time data ingestion provides data immediately for consumption in Customer Insights, until the subsequent scheduled refresh pulls this data from the data source.    
  For more information, see [Real-time data ingestion](real-time-data-ingestion.md).

- **Improvements to data preparation**
  
  Learn more about the data ingested in an entity. With the data summary, you can understand the data quality characteristics that can help to take appropriate action.    
  For more information, see [Explore entity data](entities.md#exploring-a-specific-entitys-data).

- **Ingest analytical data from Dynamics 365 with Common Data Service**
  
  Common Data Service is available as a way to create data sources in Customer Insights. Existing Dynamics 365 customers can ingest analytical entities from Common Data Service to Customer Insights. A single data source can simultaneously use the same Common Data Service-managed lake in a Customer Insights instance.    
  For more information, see [Connect to data in a Common Data Service managed data lake](connect-common-data-service-lake.md).

#### Extensibility

- **Export to LiveRamp**

  Activate your data in LiveRamp® to connect with over 500 platforms across digital, social, and TV ecosystems. Leverage your data in LiveRamp for targeting, suppressing, and personalizing ad campaigns.    
  For more information, see [LiveRamp&reg; connector](export-liveramp.md).

- **Customer Insights Teams Add-in**
  
  The bot provides lookup capabilities for unified customer profiles. It will show a card with up to 15 fields from the resulting customer profile. Multiple matches return a list of results where you can select a profile.    
  For more information, see [Teams bot for Customer Insights](export-teams-bot.md).

#### Measures

- **Measure list page**
  
  Improvements to the measures page include support for actions on a single measure and on multiple measures at once. Additionally, you'll find a search field to find and track measures quickly.    
  For more information, see [Create and manage segments](segments.md).

- **Improvements to compounded measures**
  
  Users can create, edit, and delete measures that are based on other measures. For example, a measure constructed on another measure that was constructed on a third measure.

#### Segments

- **Additional operator**
  
  The In-set operator allows segmentation for customers by several possible string values. Before this operator was added, you had to construct such segments with multiple OR conditions. The In-set operator lets you do that with a single condition.    
  For more information, see [Create and manage segments](segments.md).

#### System administration

- **Copy configuration settings to a new environment**
  
  Copy your Customer Insights configuration from one environment to another. While creating a new environment, you can select an existing environment you want to copy the configuration from. We currently support data sources, data unification, relationships, measures, and segments to be copied. Data source credentials and actual data aren't copied.    
  For more information, see [Manage environments](manage-environments.md).
