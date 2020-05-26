---
title: "New and upcoming features (Dynamics 365 Customer Insights) | Microsoft Docs"
description: "Information about new features, improvements, and bug fixes in Dynamics 365 Customer Insights releases."
ms.date: 05/26/2020
ms.service: dynamics-365-ai
ms.topic: "article"
author: m-hartmann
ms.author: mhart
ms.reviewer: midevane
manager: shellyha
---

# What's new in Dynamics 365 Customer Insights

We're excited to announce our newest updates! This article summarizes public preview features, general availability enhancements, and feature updates. To see the long-term feature plans, take a look at the [Dynamics 365 and Power Platform release plans](https://docs.microsoft.com/dynamics365/release-plans/).

We roll out updates on a region-by-region basis. So certain regions might see features before others. Unless specified differently, you don't need to take any action and we'll update the app automatically with no downtime.

> [!TIP]
> To submit and vote on feature requests and product suggestions, go to the [Dynamics 365 Application Ideas portal](https://experience.dynamics.com/ideas/categories/?forum=79a8c474-4e35-e911-a971-000d3a4f3343&forumName=Dynamics%20365%20Customer%20Insights).

## May 2020 update

The Dynamics 365 Customer Insights updates in May 2020 includes several features, performance upgrades, and bug fixes.

### New and updated features in May 2020

#### Data ingestion

- **Real-time data ingestion: history views**
- **Real-time data ingestion: profile updates**

#### Extensibility

- **Updated timeline and pagination on the Customer Card Add-in**
- **Power automate trigger for segment changes**
- **Multitenant support for custom models**

#### Measures

- **Improvements to compounded measures**

#### Segments

- **Entity path automation**
- **Actions on multiple segments**
- **Improvements to compounded segments**
- **Refresh segments**
- **Segment list page**
- **Expand segments**

#### System administration

- Customer Insights available in Microsoft Dynamics 365 Online Government

## April 2020 update

The Dynamics 365 Customer Insights updates in April 2020 includes several features, performance upgrades, and bug fixes.

### New and updated features in April 2020

#### Activities

- **Map activity entity to standard activity type**
  
  Activity configuration and storage is currently based on a static design to view them in a timeline. The semantic meaning of activities, which has potential for multiple use-cases in AI models, isn't fully used at the moment. We plan to make the activity timeline more dynamic, based on the activity type and better semantic understanding of the activities. This feature aims to identify the activity type as defined in Common Data Model for any ingested activity.

#### Data ingestion

- **Real-time data ingestion(activities)**
  
  Real-time data ingestion provides data immediately for consumption in Customer Insights, until the subsequent scheduled refresh pulls this data from the data source. For more information, see [Real-time data ingestion](https://docs.microsoft.com/dynamics365/ai/customer-insights/real-time-data-ingestion).

- **Improvements to data preparation**
  
  Learn more about the data ingested in an entity. With the data summary, you can understand the data quality characteristics that can help to take appropriate action. For more information, see [Explore entity data](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-entities#exploring-a-specific-entitys-data).

- **Ingest analytical data from Dynamics 365 with Common Data Service**
  
  Common Data Service is available as a way to create data sources in Customer Insights. Existing Dynamics 365 customers can ingest analytical entities from Common Data Service to Customer Insights. A single data source can simultaneously use the same Common Data Service-managed lake in a Customer Insights instance. For more information, see [Connect to data in a Common Data Service managed data lake (preview)](connect-common-data-service-lake.md).

#### Extensibility

- **Export to LiveRamp**

  Activate your data in LiveRamp® to connect with over 500 platforms across digital, social, and TV ecosystems. Leverage your data in LiveRamp for targeting, suppressing, and personalizing ad campaigns. For more information, see [LiveRamp&reg; connector (preview)](export-liveramp.md).

- **Customer Insights Teams Add-in**
  
  The bot provides lookup capabilities for unified customer profiles. It will show a card with up to 15 fields from the resulting customer profile. Multiple matches return a list of results where you can select a profile. For more information, see [Teams bot for Customer Insights (preview)](export-teams-bot.md).

#### Measures

- **Measure list page**
  
  Improvements to the measures page include support for actions on a single measure and on multiple measures at once. As well as the addition of a search field to find and track measures quickly.

#### Segments

- **Additional operator**
  
  The In-set operator allows segmentation for customers by several possible string values. Before this operator was added, you had to construct such segments with multiple OR conditions. The In-set operator lets you do that with a single condition.

#### System administration

- **Copy configuration settings to a new environment**
  
  Copy your Customer Insights configuration from one environment to another. While creating a new environment, you can select an existing environment you want to copy the configuration from. We currently support data sources, data unification, relationships, measures, and segments configuration to be copied. Data source credentials and actual data will not be copied. For more information, see [Manage environments](create-manage-environment.md).
