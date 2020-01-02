---
title: "Data locations for Dynamics 365 Customer Service Insights"
description: "Learn where data for Customer Service Insights is stored."
keywords: "data location"
ms.date: 10/21/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
ms.assetid: 
author: iaanw
ms.author: iawilt
manager: shellyha
search.app: capaedac-csi
search.audienceType: enduser
search.appverid: met150
---

# Where an organization's Customer Service Insights data is located

Customer Service Insights is deployed into the Microsoft Azure datacenters (also referred to as “regions”) listed below.

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

## Customer data at rest in a geographic location

Microsoft will not transfer customer data outside the selected Azure geographic location (geo) for Dynamics 365 Customer Service Insights *except* when:

- It is necessary for Microsoft to provide customer support, troubleshoot the service, or comply with legal requirements.
- Customers use services that are designed to operate globally, including the following: 
    - Email marketing to send marketing messaging globally as configured by the customer.
    - Dynamics 365 home page, which stores application names, descriptions, and logos globally for performance.
    - Azure Active Directory, which may store Active Directory data globally. More information: [What is Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-whatis)
    - Azure Multi-Factor Authentication, which may store Multi-Factor Authentication data globally. More information: [How it works: Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/active-directory/authentication/concept-mfa-howitworks).
    - Customer data collected during the onboarding process by the Microsoft Office 365 Admin Center. More information: [About the Microsoft 365 admin center](https://support.office.com/article/About-the-Office-365-Admin-Center-758befc4-0888-4009-9f14-0d147402fd23).
    - Services that provide global routing functions and do not process or store customer data. This includes Azure DNS, which provides domain name services that route to different regions; or
    - Preview, beta, or other pre-release services, which typically store customer data in the United States but may store it globally. 
    - Additionally, certain types of customer data (specifically the application name, application description, and application logo) will be stored globally, rather than in the primary storage geographic region.
- Customers configure external services to extend Dynamics 365 for Customer Service Insights. Such customer configurations may cause customer data to be transferred outside of the selected geographic region. Examples of customer configurable external services include: 
  - **Machine Learning Cognitive Services:** If features that use cognitive services are activated, customer data for domains such as product recommendations and demand forecasting can be synchronized outside of the configured region. Use of these features is optional. More information: [Tutorial: Recommendations solution](https://azure.microsoft.com/services/cognitive-services/recommendations/).
  - **Data integration:** Configuration of Customer Service Insights data management features that work with external services (whether provided by Microsoft or a third party) may result in the transfer of core customer data outside of the region configured for the production environment to a geographic location that customers designate. More information: [Choose a data integration (import/export) strategy](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/integration-overview).
  - **Microsoft Power BI, Microsoft Power Apps, Power Automate and Power Virtual Agents:** Customers who connect their Power BI, Power Apps,  Power Automate, or Power Virtual Agents deployment to Customer Service Insights may send customer data outside of the designated region to the geographic area where their Power BI, Power Apps, Power Automate, or Power Virtual Agents service is deployed. More information: [Microsoft Trust Center: Data locations](https://www.microsoft.com/TrustCenter/CloudServices/business-application-platform/data-location).
  - **Microsoft Visual Studio Team Services:** Customers can choose where to store custom code, metadata, and data assets that support their Dynamics 365 Customer Service Insights implementation. More information: [Products available by region](https://azure.microsoft.com/regions/services/?v=17.42n).
  - **Dynamics 365 apps geo-to-geo migration:** Customers can request to change the geographic location of their Dynamics 365 environments by doing a geo-to-geo migration. However, this action will not automatically migrate Dynamics 365 Customer Service Insights workspaces created before the geo-to-geo migration. As a result, such workspaces may be in a different geographic location than an organization's other Dynamics 365 data. Workspaces created after the geo-to-geo migration will be located in the same region as the other Dynamics 365 apps' environments. More information: [Geo to geo migrations](https://go.microsoft.com/fwlink/?linkid=2105275) in the Power Platform documentation library.
  - **New geographic location for Dynamics 365 Customer Service Insights data:** If a new Dynamics 365 Customer Service Insights geographic location is introduced in the same geographic location as your Dynamics 365 environment, then Microsoft will perform a manual geo-to-geo migration on your behalf to store your organization's Dynamics 365 Customer Service Insights data to the same geographic location as your Dynamics 365 apps environment. However, if a workspace has not been accessed for over 30 days, then the migration will not be completed and your organization's Dynamics 365 Customer Service Insights data will not be stored in the same geographic location.  
