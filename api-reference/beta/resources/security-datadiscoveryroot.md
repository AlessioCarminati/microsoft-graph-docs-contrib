---
title: "dataDiscoveryRoot resource type"
description: "Provides data about discovery report entities"
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: resourcePageType
---

# dataDiscoveryRoot resource type

Namespace: microsoft.graph.security

Provides data about discovery report entities.

Inherits from [microsoft.graph.entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List dataDiscoveryReport](../api/security-datadiscoveryroot-list-cloudappdiscovery.md)|[microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md) collection|Get the dataDiscoveryReport resources 

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**These are the available properties** Inherited from [microsoft.graph.entity](../resources/entity.md).|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|microsoft.graph.security.cloudAppDiscovery|[microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md)|**These are the available relationships**|

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.security.dataDiscoveryRoot",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.dataDiscoveryRoot",
  "id": "String (identifier)"
}
```

