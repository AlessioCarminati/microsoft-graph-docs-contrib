---
title: "userCloudLicensing resource type"
description: "Represents a user's relationships to Cloud Licensing resources."
author: "patrick-starrin"
ms.localizationpriority: medium
doc_type: resourcePageType
---

# userCloudLicensing resource type

Namespace: microsoft.graph.cloudLicensing

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents a user's relationships to Cloud Licensing resources.

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List usageRights](../api/cloudlicensing-usercloudlicensing-list-usagerights.md)|[microsoft.graph.cloudLicensing.usageRight](../resources/cloudlicensing-usageright.md) collection|Get a list of the [microsoft.graph.cloudLicensing.usageRight](../resources/cloudlicensing-usageright.md) objects granted to the user.|
|[Get usageRight](../api/cloudlicensing-usercloudlicensing-get-usageright.md)|[microsoft.graph.cloudLicensing.usageRight](../resources/cloudlicensing-usageright.md)|Read the properties and relationships of a [microsoft.graph.cloudLicensing.usageRight](../resources/cloudlicensing-usageright.md) object granted to the user.|

## Properties
None.

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|usageRights|[microsoft.graph.cloudLicensing.usageRight](../resources/cloudlicensing-usageright.md) collection|The rights of the user to use various services, granted by the combination of their assigned licenses.|

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.cloudLicensing.userCloudLicensing"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.cloudLicensing.userCloudLicensing"
}
```
