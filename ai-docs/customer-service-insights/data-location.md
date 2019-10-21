---
title: "Data locations for Dynamics 365 Customer Service Insights"
description: "Learn about the regions where data for Customer Service Insights is stored."
keywords: "data location"
ms.date: 07/10/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: m-hartmann
ms.author: mhart
manager: shellyha
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Where an organization's Customer Service Insights data is located

Customer Service Insights can be deployed into the Microsoft Azure datacenters (also referred to as “regions”) listed below.

Microsoft may replicate customer data to other regions available within the same geography for data durability, except as specified below. No matter where customer data is stored, Microsoft does not control or limit the locations from which customers or their end users may access customer data.

## Data locations

| Azure geographic areas (geos) | Azure datacenters (regions)               |
|-------------------------------|-------------------------------------------|
|    Europe                     |    West Europe (Netherlands)              |
|                               |    North Europe (Ireland)                 |
|                               |                                           |
|    United States              |    East US (Blue Ridge, VA)               |
|                               |    South Central US (Des Moines, IA)      |
|                               |    West US (Quincy, WA)                   |
|                               |                                           |
|    Australia                  |    Australia East (New South   Wales)     |
|                               |    Australia Southeast   (Victoria)       |
|                               |                                           |
|    Asia Pacific               |    Southeast Asia (Singapore)             |
|                               |    East Asia (Hong Kong)                  |
|                               |                                           |
|    United Kingdom             |    UK South (London)                      |
|                               |    UK West (Cardiff, Durham)              |
|                               |                                           |
|    Brazil                     |    Brazil South (São Paulo State)<sup>1</sup>|
|                               |                                           |
|    Canada                     |    Canada Central (Toronto)               |
|                               |    Canada East (Québec City)              |
|                               |                                           |
|    India                      |    Central India (Pune)                   |
|                               |    South India (Chennai)                  |
|                               |                                           |
|    Japan                      |    Japan East (Tokyo, Saitama)            |
|                               |    Japan West (Osaka)                     |
| | |
| France | France Central (Paris) |
| | Framce South (Marseille) |

<sup>1 Because there is only one region in Brazil, customer data in Brazil South may be replicated to South Central US (Texas) for disaster recovery purposes. </sup>

## Customer data at rest in geo

Microsoft will not transfer customer data outside the selected Azure geographic location (geo) for Dynamics 365 Customer Service Insights except when:

- It is necessary for Microsoft to provide customer support, troubleshoot the service, or comply with legal requirements.
- Customers use services that are designed to operate globally, including the following: 
    - Email marketing sending used to send marketing messaging globally as configured by the customer.
    - Dynamics 365 home page, which stores application names, descriptions, and logos globally for performance
    - Azure Active Directory, which may store Active Directory data globally. You can find more information [here](https://docs.microsoft.com/azure/active-directory/active-directory-whatis).
    - Azure Multi-Factor Authentication, which may store Multi-Factor Authentication data globally. You can find more information [here](https://azure.microsoft.com/services/multi-factor-authentication/).
    - Customer data collected during the onboarding process by the Microsoft Office 365 Admin Center. You can find more information [here](https://support.office.com/article/About-the-Office-365-Admin-Center-758befc4-0888-4009-9f14-0d147402fd23).
    - Services that provide global routing functions and do not process or store customer data. This includes Azure DNS, which provides domain name services that route to different regions; or
    - Preview, beta, or other pre-release services, which typically store customer data in the United States but may store it globally. 
    - Additionally, certain types of customer data (specifically the application name, application description, and application logo) will be stored globally, rather than in the primary storage geo.
- Customers configure external services to extend Dynamics 365 for Customer Service Insights such customer configurations may cause customer data to be transferred outside of the selected geo. Examples of customer configurable external services include: 
  - **Machine Learning Cognitive Services:** If features that use cognitive services are activated, customer data for domains such as product recommendations and demand forecasting can be synchronized outside of the configured region. Use of these features is optional. You can find more information [here](https://azure.microsoft.com/services/cognitive-services/recommendations/).
  - **Data integration:** Configuration of Dynamics 365 for Customer Service Insights data management features that work with external services (whether provided by Microsoft or a third party) may result in the transfer of core customer data outside of the region configured for the production environment to a geographic location that customers designate. You can find more information [here](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/integration-overview).
  - **Microsoft Power BI, Microsoft PowerApps, and Microsoft Flow:** Customers who connect their Power BI, PowerApps, or Flow deployment to Dynamics 365 for Customer Service Insights may send customer data outside of the designated region to the geographic area where their Power BI, PowerApps, or Flow is deployed. You can find more details [here](https://www.microsoft.com/TrustCenter/CloudServices/business-application-platform/data-location).
  - **Microsoft Visual Studio Team Services:** Customers can choose where to store custom code, metadata, and data assets that support their Dynamics 365 for Customer Service Insights implementation. You can find more information about the availability of Visual Studio Team Services [here](https://azure.microsoft.com/regions/services/?v=17.42n).
  - **Dynamics 365 apps geo to geo migration:** Customers can request to change the geo location of their Dynamics 365 app environments by doing a geo to geo migration. However, this action will not automatically migrate your Dynamics 365 Customer Service Insights workspaces created *before* the geo to geo migration. As a result, such workspaces may be in a different geo location than your other Dynamics 365 apps' data. Workspaces created *after* the geo to geo migration will be in the same region as the rest of your Dynamics 365 apps' environments. You can find more information [at the Geo to geo migration article](https://go.microsoft.com/fwlink/?linkid=2105275) in the Power Platform data center library.
  - **New geo location for Dynamics 365 Customer Service Insights data:** If a new Dynamics 365 Customer Service Insights geo location is introduced in the same geo as your Dynamics 365 app's environment, then Microsoft will perform a manual geo to geo migration on your behalf to store your Dynamics 365 Customer Service Insights data in the same geo as your Dynamics 365 app's environment. However, if your workspace has not been logged into for over 30 days, then the migration will not be completed successfully and your Dynamics 365 Customer Service Insights data will not be stored in the same geo.  
