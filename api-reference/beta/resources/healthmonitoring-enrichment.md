---
title: "enrichment resource type"
description: "Represent a set of properties that add context to the alert."
author: "huatang92"
ms.localizationpriority: medium
ms.subservice: "entra-health-monitoring"
doc_type: resourcePageType
---

# enrichment resource type

Namespace: microsoft.graph.healthMonitoring

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represent a set of properties that add context to the alert.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|impacts|[microsoft.graph.healthMonitoring.resourceImpactSummary](../resources/healthmonitoring-resourceimpactsummary.md) collection|A collection of resourceImpactSummary that gives a high level view of what kind of resources were impacted and to what degree.|
|state|microsoft.graph.healthMonitoring.enrichmentState|Indicates if the alert has been enriched with additional data..The possible values are: `none`, `inProgress`, `enriched`, `unknownFutureValue`.|
|supportingData|[microsoft.graph.healthMonitoring.supportingData](../resources/healthmonitoring-supportingdata.md)|A collection of supportingData locations that can be queried for debugging the alert.|

## Relationships
None.

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.healthMonitoring.enrichment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.healthMonitoring.enrichment",
  "state": "String",
  "impacts": [
    {
      "@odata.type": "microsoft.graph.healthMonitoring.userImpactSummary"
    }
  ],
  "supportingData": {
    "@odata.type": "microsoft.graph.healthMonitoring.supportingData"
  }
}
```

