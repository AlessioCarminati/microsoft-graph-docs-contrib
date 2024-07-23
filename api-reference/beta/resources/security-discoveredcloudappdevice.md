---
title: "discoveredCloudAppDevice resource type"
description: "Get the details of the devices that are accessing discovered cloud apps."
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: resourcePageType
---

# discoveredCloudAppDevice resource type

Namespace: microsoft.graph.security

Get the details of the devices that are accessing discovered cloud apps.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List](../api/security-endpointdiscoveredcloudappdetail-list-devices.md)|[microsoft.graph.security.discoveredCloudAppDevice](../resources/security-discoveredcloudappdevice.md) collection|Get a list of the discovered cloud apps devices.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|name|String|The name of cloud app.|

## Relationships
None.

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "name",
  "@odata.type": "microsoft.graph.security.discoveredCloudAppDevice",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.discoveredCloudAppDevice",
  "name": "String (identifier)"
}
```

