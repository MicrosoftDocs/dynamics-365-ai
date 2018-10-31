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

**When it comes to Customer 360**, currently there are several types of APIs that you can start utilizing. The details (parameters, responses, etc) of these APIs can be found in the **Customer 360 Swagger Webpage:**

https://dxt-wus-01.api.ci.ai.dynamics.com/swagger/index.html
https://idratherbewriting.com/learnapidoc/pubapis_swagger.html

[APIs image 1]

**The goal of this section**, however, is **not to cover all** the Customer 360 APIs but rather to:
- Provide a guidance as for how to use the Swagger tool
- Provide explainations around some of the most important functionalities that you, as a user, can leverage through our APIs

### How to Use the Customer 360 Swagger Webpage
If you are not familiar with Swagger, you can explore the following step-by-step tutorials:

https://idratherbewriting.com/learnapidoc/pubapis_swagger.html
https://idratherbewriting.com/learnapidoc/pubapis_swagger.html

### Functionalities served with the Customer 360 *Open Data Protocol APIs*:

[API image 2]

- *Put* API: **/api/instances/{instanceId}/data/{relativePath}**

|Functionality  |Guidance  |Limitations   |
|---------|---------|---------|
|Export any ingested dataset including the Master Customer Dataset that was created during the data configuration process
(JSON/csv formats)
     |Use $Search command with content-type: text/csv header as explained here:
https://www.odata.org/getting-started/basic-tutorial/
         |1. Can be done only if Customer ID is present in the queried dataset, 2. Can not be executed along with functionalities 2-5

|2     |Attribute type         |
|3    |Operator         |
|4    |Value         |

### Limitations involved with using the Customer 360 *Conflation APIs*: 

[APIs image 3]

**Limitations by field (across all Conflation APIs):

[API table 2]

**Additional limitations by API:**

[API table3]

//Viewing and retrieving configurations that were made during the *Data Configuration* process 
//and can do the conflation here
//and configure 


### Limitations ivolved with using the Customer 360 *Relationship APIs*: 

//management API for relationship: ? 
//notes: you can use the relationship in the segment query builder

[APIs image 4]

**Limitations Common to all APIs**:
**First**, these APIs require that data has already been ingested, except for the following APIs:
- GET /api/instances/{instanceId}/manage/schema/entitySemanticLabels
- GET /api/instances/{instanceId}/manage/schema/attributeSemanticLabels
- GET /api/instances/{instanceId}/manage/relationships
- GET /api/instances/{instanceId}/manage/relationships/{relationshipName}
- DELETE /api/instances/{instanceId}/manage/relationships/{relationshipName}

**Second**, specifically for relationship APIs, any time {relationshipName} is provided, there must actually exist a relationship with that name in the given instance.

**Additional limitations by API**:

[API table 4]

### Functionalities served with the Customer 360 *Segmentation APIs*: 
management API for segments: Create, update, get and delete segment definition. Activste and deactivate. 
query API: get customers part of a segment (/data/Customer?$filter=IsMemberOfSegment(segmentname))
search and query customer data  /data/Customer(customerId='123')

[APIs image 5]

- **Functionalities and limitations by API:**

[API table 5]
