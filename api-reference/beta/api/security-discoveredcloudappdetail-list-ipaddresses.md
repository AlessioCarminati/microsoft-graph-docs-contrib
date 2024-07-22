---
title: "List ipAddresses"
description: "Get the discoveredCloudAppIPAddress resources from the ipAddresses navigation property."
author: "nechamam"
ms.localizationpriority: medium
ms.subservice: "security"
doc_type: apiPageType
---

# List ipAddresses

Namespace: microsoft.graph.security

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the discoveredCloudAppIPAddress resources from the ipAddresses navigation property.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "security-discoveredcloudappdetail-list-ipaddresses-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/security-discoveredcloudappdetail-list-ipaddresses-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /security/dataDiscovery/cloudAppDiscovery/uploadedStreams/{cloudAppDiscoveryReportId}/microsoft.graph.security.aggregatedAppsDetails(period=duration'{duration}')/{appId}/ipAddresses
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

If successful, this method returns a `200 OK` response code and a collection of [discoveredCloudAppIPAddress](../resources/security-discoveredcloudappipaddress.md) objects in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_discoveredcloudappipaddress"
}
-->
``` http
GET https://graph.microsoft.com/beta/discoveredCloudAppDetail/ipAddresses
```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.security.discoveredCloudAppIPAddress)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.security.discoveredCloudAppIPAddress",
      "ipAddress": "28827319-0708-fbb2-d5e4-7f5a908fe599"
    }
  ]
}
```

