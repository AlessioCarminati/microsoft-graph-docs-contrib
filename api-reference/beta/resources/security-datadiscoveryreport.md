---
title: "dataDiscoveryReport resource type"
description: "Describes the discovery report resource"
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: resourcePageType
---

# dataDiscoveryReport resource type

Namespace: microsoft.graph.security

Describes the discovery report resource.

Inherits from [microsoft.graph.entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List](../api/security-datadiscoveryroot-list-cloudappdiscovery.md)|[microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md) collection|Get a list of the [microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md) objects and their properties.|
|[Get](../api/security-datadiscoveryreport-get.md)|[microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md)|Read the properties and relationships of a [microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md) object.|
|[List uploadedStreams](../api/security-datadiscoveryreport-list-uploadedstreams.md)|[microsoft.graph.security.cloudAppDiscoveryReport](../resources/security-cloudappdiscoveryreport.md) collection|Get the cloudAppDiscoveryReport resources from the uploadedStreams navigation property.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**These are all the available properties.** Inherited from [microsoft.graph.entity](../resources/entity.md).|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|uploadedStreams|[microsoft.graph.security.cloudAppDiscoveryReport](../resources/security-cloudappdiscoveryreport.md) collection|**These are all the available upload streams**|

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.security.dataDiscoveryReport",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.dataDiscoveryReport",
  "id": "String (identifier)"
}
```

