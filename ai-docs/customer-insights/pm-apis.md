---
title: "APIs | MicrosoftDocs"
description: Text to go here
ms.custom: ""
ms.date: 10/1/2018
ms.reviewer: ""
ms.service: "dynamics-365-ai"
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
applies_to: 
  - "Dynamics 365 (online)"
  - "Dynamics 365 Version 9.x"
ms.assetid: 
caps.latest.revision: 31
author: "jimholtz"
ms.author: "jimholtz"
manager: "kvivek"
robots: noindex,nofollow
---
# APIs
*Note: this is a technical documentation. While it's purpose is to serve all users who wish to leverage the Customer 360 APIs, it might be most valuable for technical users.

[!INCLUDE [cc-beta-prerelease-disclaimer](../includes/cc-beta-prerelease-disclaimer.md)]

**When it comes to Customer 360**, currently there are several types of APIs that you can start utilizing. The details of all our current APIs can be found in the following Swagger webpage:

https://dxt-wus-01.api.ci.ai.dynamics.com/swagger/index.html
https://idratherbewriting.com/learnapidoc/pubapis_swagger.html

[APIs image 1 - Swagger page]

**The goal of this section**, however, is **not to cover all** the Customer 360 APIs but rather to:
- Provide a guidance as for how to use the Swagger tool
- Provide further explainations on the Customer 360 APIs that you, as a user, are expected to use the most

### How to Use the Customer 360 Swagger Webpage
If you are not familiar with Swagger, you can explore the following step-by-step tutorials:

https://idratherbewriting.com/learnapidoc/pubapis_swagger.html


### Using *Open Data Protocol APIs* for: Accessing Customer 360 data
customer master dataset
any data that was ingested
search and query customer data  /data/Customer(customerId='123')
filter and search only for the customer entity
related entities to the customer - can be user to export (csv/json) all the above - can only be found if customer ID is used (one of the two)

### Using *Conflation APIs* for: Viewing and retrieving configurations that were made during the *Data Configuration* process 
and can do the conflation here
and configure 
patrick

### Using *Relationship APIs* for: 
management API for relationship: ? 
notes: you can use the relationship in the segment query builder

### Using *Segmentation APIs* for: 
management API for segments: Create, update, get and delete segment definition. Activste and deactivate. 
query API: get customers part of a segment (/data/Customer?$filter=IsMemberOfSegment(segmentname))


