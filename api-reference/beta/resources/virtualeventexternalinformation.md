---
title: "virtualEventExternalInformation resource type"
description: "Represents the external information for a virtual event."
author: "halleclottey-msft"
ms.localizationpriority: medium
ms.subservice: "cloud-communications"
doc_type: resourcePageType
---

# virtualEventExternalInformation resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the external information for a [virtual event](../resources/virtualevent.md).

## Properties

|Property|Type|Description|
|:---|:---|:---|
|applicationId|String| TODO: PLACEHOLDER DESCRIPTION. READ ONLY.|
|externalEventId|String| TODO: PLACEHOLDER DESCRIPTION i.e. The identifier for a **virtualEventExternalInformation** object. Optional. If set, the maximum supported length is 256 characters.|

## Relationships

|Relationship|Type|Description|
|:---|:---|:---|
|virtualEvents|[virtualEvent](../resources/virtualevent.md)| Provides external information for a [virtual event](../resources/virtualevent.md).|

## JSON representation

The following JSON representation shows the resource type.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.virtualEventExternalInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.virtualEventExternalInformation",
  "applicationId": "String",
  "externalEventId": "String"
}
```

## Related content

- [Virtual event](../resources/virtualevent.md)
- [Virtual event townhalls](../resources/virtualeventtownhall.md)
- [Virtual event webinars](../resources/virtualeventwebinar.md)
