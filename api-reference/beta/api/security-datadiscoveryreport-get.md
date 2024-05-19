---
title: "Get dataDiscoveryReport"
description: "Read the properties and relationships of a microsoft.graph.security.dataDiscoveryReport object."
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: apiPageType
---

# Get dataDiscoveryReport

Namespace: microsoft.graph.security

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "security-datadiscoveryreport-get-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/security-datadiscoveryreport-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /dataDiscoveryRoot/cloudAppDiscovery
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

If successful, this method returns a `200 OK` response code and a [microsoft.graph.security.dataDiscoveryReport](../resources/security-datadiscoveryreport.md) object in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "get_datadiscoveryreport"
}
-->
``` http
GET https://graph.microsoft.com/beta/dataDiscoveryRoot/cloudAppDiscovery
```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.security.dataDiscoveryReport"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.security.dataDiscoveryReport",
    "id": "ba776378-53ea-ab5a-8278-3b1e63fdaa38"
  }
}
```

