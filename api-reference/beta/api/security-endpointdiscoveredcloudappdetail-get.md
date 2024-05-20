---
title: "Get endpointDiscoveredCloudAppDetail"
description: "Read the properties and relationships of a microsoft.graph.security.endpointDiscoveredCloudAppDetail object."
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: apiPageType
---

# Get endpointDiscoveredCloudAppDetail

Namespace: microsoft.graph.security

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [microsoft.graph.security.endpointDiscoveredCloudAppDetail](../resources/security-endpointdiscoveredcloudappdetail.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "security-endpointdiscoveredcloudappdetail-get-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/security-endpointdiscoveredcloudappdetail-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
```

## Optional query parameters

This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [microsoft.graph.security.endpointDiscoveredCloudAppDetail](../resources/security-endpointdiscoveredcloudappdetail.md) object in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "get_endpointdiscoveredcloudappdetail"
}
-->
``` http

```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.endpointDiscoveredCloudAppDetail"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.security.endpointDiscoveredCloudAppDetail",
    "id": "bd2f8b64-d13c-d383-1c05-649d4a628a65",
    "displayName": "String",
    "tags": [
      "String"
    ],
    "riskScore": "Integer",
    "uploadNetworkTrafficInBytes": "Integer",
    "downloadNetworkTrafficInBytes": "Integer",
    "transactionCount": "Integer",
    "ipAddressCount": "Integer",
    "userCount": "Integer",
    "lastSeenDateTime": "String (timestamp)",
    "domains": [
      "String"
    ],
    "category": "String",
    "deviceCount": "Integer"
  }
}
```

