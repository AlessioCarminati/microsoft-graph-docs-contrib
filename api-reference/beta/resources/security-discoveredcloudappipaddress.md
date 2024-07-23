---
title: "discoveredCloudAppIPAddress resource type"
description: "Get details of IP addresses accessing discovered cloud app."
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: resourcePageType
---

# discoveredCloudAppIPAddress resource type

Namespace: microsoft.graph.security

Get details of IP addresses accessing discovered cloud app.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List](../api/security-discoveredcloudappdetail-list-ipaddresses.md)|[microsoft.graph.security.discoveredCloudAppIPAddress](../resources/security-discoveredcloudappipaddress.md) collection|Get a list of the discovered apps and the IP addresses that are accessing the cloud app.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|ipAddress|String|The IpAddresses accessed by discovered cloud app.|

## Relationships
None.

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "keyProperty": "ipAddress",
  "@odata.type": "microsoft.graph.security.discoveredCloudAppIPAddress",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.security.discoveredCloudAppIPAddress",
  "ipAddress": "String (identifier)"
}
```

