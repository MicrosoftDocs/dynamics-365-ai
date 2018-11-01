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

**When it comes to Customer 360**, currently there are several types of APIs that you can start utilizing. The details (parameters, responses, etc) of these APIs can be found in the [Customer 360 Swagger webpage](https://dxt-cuseaup-01.api.ci.ai.dynamics.com/swagger/index.html).

> [!div class="mx-imgBorder"] 
> ![](media/api-swagger-install.png "Customer 360 Swagger webpage")

The goal of this section is not to cover all the Customer 360 APIs but rather to:

- Provide guidance for how to use the Swagger tool
- Provide explanations around some of the most important functionalities that you, as a user, can leverage through our APIs

## How to use the Customer 360 Swagger webpage
If you are not familiar with Swagger, see the following step-by-step tutorial: [Swagger UI tutorial](https://idratherbewriting.com/learnapidoc/pubapis_swagger.html).

## Functionalities served with the Customer 360 Open Data Protocol APIs

> [!div class="mx-imgBorder"] 
> ![](media/api-entity-data.png "Open Data Protocol APIs")

- *Put* API: /api/instances/{instanceId}/data/{relativePath}


|Functionality  |Guidance  |Limitations  |
|---------|---------|---------|
|1. **Export** any ingested dataset including the Master Customer Dataset that was created during the data configuration process (JSON/csv formats)     | Use **$Search** command with conte-type: text/csv header. For more information, see [Basic Tutorial](https://www.odata.org/getting-started/basic-tutorial/).        |1. Can be done only if **Customer ID** is present in the queried dataset<br/>2. Can't be executed along with functionalities 2-5         |
|2. **Search and query** the Master Customer Dataset that was created during the data configuration process      | Use the **$Search** command. For more information, see [Basic Tutorial](https://www.odata.org/getting-started/basic-tutorial/).        | Currently not available.        |
|3. **Filter** the Master Customer Dataset     | Use the **$Filter** command. For more information, see [Basic Tutorial](https://www.odata.org/getting-started/basic-tutorial/).       | Currently not available.        |
|4. **Search and query** other ingested datasets     | Use the **$Search** command. For more information, see [Basic Tutorial](https://www.odata.org/getting-started/basic-tutorial/).         | 1. Can be done on if **Customer ID** is present in the queried dataset<br/>2. Can't be executed along with 1      |
|5. **Filter** other ingested datasets     |Use the **$Filter** command. For more information, see [Basic Tutorial](https://www.odata.org/getting-started/basic-tutorial/).           | 1. Can be done on if **Customer ID** is present in the queried dataset<br/>2. Can't be executed along with 1          |

## Limitations involved with using the Customer 360 conflation APIs

See the **Conflation** table in the [Customer 360 Swagger webpage](https://dxt-cuseaup-01.api.ci.ai.dynamics.com/swagger/index.html).

###Limitations by field (across all Conflation APIs)

|Field  |Limitation  |
|---------|---------|
|{instanceId}     | Id must be the Id of an existing instance, and the user issuing the request must have access to that instance         |
|{entityName}     | It should be an entity name that has data ingested for the given instance (and a data source, if that is given as well)        |
|{datasourceId}     | Id must be the Id of a data source that exists inside of the given instance        |
|{conflationId}     | Id must be the Id of an existing conflation for the given instance        |


### Additional limitations by API


|API  |Limitations |
|---------|---------|
|PATCH<br/>/api/instances/{instanceId}/conflations/{conflationId}/entityInformation   | 1. Request body will have a list of entity names, per datasource. These must actually exist as ingested entities for the datasource.<br/>2. Each entity named in request body must already have a primary key defined.      |
|PATCH<br/>/api/instances/{instanceId}/conflations/{conflationId}/entityInformation/{entityName}     | Same limitations as above EXCEPT the request body will have a single entity name, not a list        |
|PATCH<br/>/api/instances/{instanceId}/conflations/{conflationId}/datasources/{datasourceId}/entityInformation/{entityName}     | Same limitations as above     |
|PATCH<br/>/api/instances/{instanceId}/conflations/{conflationId}/conflationPlan     |1. Any entity that appears in the plan must have been ingested in the referenced datasource. <br/>2. Any attribute that appears in the plan must actually exist as an attribute as the referenced entity.<br/>3. Any entity that appears in the plan must have a primary key defined.<br/>4. All entities in the ConflationOrder must have corresponding EntityConflationInformation<br/>5. At least 1 rule and criteria must be defined<br/>6. No copy criteria may be included in the plan<br/>7. All entities in the plan must appear in the entity conflation order<br/>8. Entities cannot appear in the plan out of the order defined in ConflationOrder<br/>9. All matched attributes must have the same type   |
|PATCH<br/>/api/instances/{instanceId}/conflations/{conflationId}/conflictResolutionRules     |1. same as above<br/>2. same as above<br/>3. same as above<br/>4. At least 1 resolution policy must be defined against at least 1 source attribute<br/>5. All entities defined in the resolution policy must be part of the conflation plan     |


## Limitations involved with using the Customer 360 *Relationship APIs 

See the **EntityMetadata** table in the [Customer 360 Swagger webpage](https://dxt-cuseaup-01.api.ci.ai.dynamics.com/swagger/index.html).

### Limitations Common to all APIs

**First**, these APIs require that data has already been ingested, except for the following APIs:

- GET /api/instances/{instanceId}/manage/schema/entitySemanticLabels
- GET /api/instances/{instanceId}/manage/schema/attributeSemanticLabels
- GET /api/instances/{instanceId}/manage/relationships
- GET /api/instances/{instanceId}/manage/relationships/{relationshipName}
- DELETE /api/instances/{instanceId}/manage/relationships/{relationshipName}

**Second**, specifically for relationship APIs, any time {relationshipName} is provided, there must actually exist a relationship with that name in the given instance.

### Additional limitations by API

|API  |Limitations  |
|---------|---------|
|PATCH<br/>/api/instances/{instanceId}/manage/datasources/{datasourceId}/entities/entityInfo     | 1. Request body will have a list of entity names. These must all have been ingested into the given datasource.<br/>2. Request body will have a list of attribute names associated with each entity. These must actually exist as attributes of the entity.<br/>3. The ONLY allowed values for “EntityType” are “Activity” and “Unspecified”<br/>4. If EntityType  == Activity, then the entity with this EntityType must have a relationship to an entity with type Profile<br/>5. If the TimestampFieldName is provided for an entity, this must be the name of one of the attributes of that entity. That attribute must have type DateTime or long.  |
|PATCH<br/>/api/instances/{instanceId}/manage/datasources/{datasourceId}/entities/{entityName}/entityInfo     | 1. Same as above, but for a single entity rather than a list<br/>2. Same as above<br/>3. Same as above<br/>4. Same as above<br/>5. Same as above      |
|PATCH<br/>/api/instances/{instanceId}/manage/relationships     |1. Relationship name can only include letters, numbers, and underscores<br/>2. Relationship name must be unique<br/>3. Cardinality can ONLY have two values: “OneToMany”, and “ManyToOne”<br/>4. There are ONLY 4 possible relationship types: SingleKeyRelationshipOrigin, SingleKeyRelationshipDestination, DataSourceLineageOrigin, DataSourceLineageDestination<br/>5. Both the FromEntity and ToEntity must be the names of entities that actually exist in the instance<br/>6. Both the FromAttribute and ToAttribute must actually exist as attributes of the FromEntity and ToEntity    |
|PATCH<br/>/api/instances/{instanceId}/manage/relationships/{relationshipName}     |Same limitation as above EXCEPT #2 is not a limitation here, since the name was already validated during creation (whereas this is an update)         |

## Functionalities served with the Customer 360 *Segmentation APIs

management API for segments: Create, update, get and delete segment definition. Activate and deactivate. 
query API: get customers part of a segment (/data/Customer?$filter=IsMemberOfSegment(segmentname))
search and query customer data  /data/Customer(customerId='123')

See the **SegmentManagement** table in the [Customer 360 Swagger webpage](https://dxt-cuseaup-01.api.ci.ai.dynamics.com/swagger/index.html).

## Functionalities and limitations by API

|Table5  |Column2  |
|---------|---------|
|Row1     |         |
|Row2     |         |
|Row3     |         |
|Row4     |         |
|Row5     |         |
