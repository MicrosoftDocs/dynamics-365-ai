---
title: "msdyn_ConnectSequence Action | MicrosoftDocs"
description: ""
ms.date: 05/08/2020
author: susikka
ms.author: susikka
manager: shujoshi
---

# msdyn_ConnectSequence Action

Assigns a lead and opportunity entity record to a sequence.

## Parameters

|Name |Description |
|-----|-----|
|`RegardingEntityId`|Unique identifier of the entity record that is to be assigned to the sequence.|
|`RegardingEntityName`|Logical name of the entity|
|`CadenceId`|Unique identifier of the sequence|

## Example

```json
POST [Organization URI]/api/data/v9.1/msdyn_ConnectSequence

{
    "RegardingEntityId":"03468c60-6d5b-ea11-a811-000d3a54419d",
    "RegardingEntityName":"lead",
    "CadenceId":"BCEC0282-7A58-EA11-A811-000D3A54419D"
}
```

## See also

[Enable and configure the Sales accelerator](../enable-configure-sales-accelerator.md)