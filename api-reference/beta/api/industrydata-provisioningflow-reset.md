---
title: "provisioningFlow: reset"
description: "Reset a provisioningFlow."
author: "dakelle"
ms.localizationpriority: medium
ms.subservice: "industry-data-etl"
doc_type: apiPageType
---

# provisioningFlow: reset

Namespace: microsoft.graph.industryData

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Reset a [provisioningFlow](../resources/industrydata-provisioningflow.md). This action reprovisions all current data as if it were the initial run, and clears out the existing errors associated with the flow.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "industrydata-provisioningflow-reset-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/industrydata-provisioningflow-reset-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /external/industryData/outboundProvisioningFlowSets/{outboundProvisioningFlowSetId}/provisioningFlows/{provisioningFlowId}/reset
```

## Request headers

| Name         | Description               |
| :----------- | :------------------------ |
| Authorization| Bearer {token}. Required. |

## Request body

Don't supply a request body for this method.

## Response

If successful, this action returns a `202 Accepted` response code.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "provisioningflowthis.reset"
}
-->
``` http
POST https://graph.microsoft.com/beta/external/industryData/outboundProvisioningFlowSets/8c33d025-5e64-4550-2aa3-08dc4ac66fca/provisioningFlows/51f99e09-bdc5-47ff-7a0a-08dc4ac74cf1/reset
```


### Response

The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 202 Accepted
```

