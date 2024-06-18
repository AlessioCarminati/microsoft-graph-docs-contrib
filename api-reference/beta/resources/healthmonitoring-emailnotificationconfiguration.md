---
title: "emailNotificationConfiguration resource type"
description: "Represents the email configuration of an alert type defining behavior that occurs when an alert is created."
author: "huatang92"
ms.localizationpriority: medium
ms.subservice: "entra-monitoring-health"
doc_type: resourcePageType
---

# emailNotificationConfiguration resource type

Namespace: microsoft.graph.healthMonitoring

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Represents the email configuration of an alert type defining behavior that occurs when an alert is created.

## Properties
|Property|Type|Description|
|:---|:---|:---|
|groupId|String|The identifier of the group to send an email to.|
|isEnabled|Boolean|Flag indicating if email notifications are enabled on the alert type.|

## Relationships
None.

## JSON representation
The following JSON representation shows the resource type.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.healthMonitoring.emailNotificationConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.healthMonitoring.emailNotificationConfiguration",
  "groupId": "String",
  "isEnabled": "Boolean"
}
```

