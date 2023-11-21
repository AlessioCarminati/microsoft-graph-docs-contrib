---
title: "Get filteringPolicyLink"
description: "Get a filteringPolicyLink object."
author: Moti-ba
ms.localizationpriority: medium
ms.prod: global-secure-access
doc_type: apiPageType
---

# Get filteringPolicyLink
Namespace: microsoft.graph.networkaccess

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a [filteringPolicyLink](../resources/networkaccess-filteringpolicylink.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|NetworkAccessPolicy.Read.All,NetworkAccessPolicy.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

[!INCLUDE [rbac-global-secure-access-apis-read](../includes/rbac-for-apis/rbac-global-secure-access-apis-read.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /networkaccess/filteringPolicies/{filteringPoliciesId}
```

## Optional query parameters
This method does not support OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [microsoft.graph.networkaccess.filteringPolicyLink](../resources/networkaccess-filteringpolicylink.md) object in the response body.

## Examples

### Request
The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "get_filteringpolicylink"
}
-->
``` http
GET https://graph.microsoft.com/beta/networkaccess/filteringPolicies/bb4e13cd-656b-499a-929f-d16bf16951ba?$expand=policyRules
```


### Response
The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.networkaccess.filteringPolicyLink"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#networkAccess/filteringProfiles('9020f79d-71f6-4650-83a9-6b532479578f')/policies",
    "value": [
        {
            "@odata.type": "#microsoft.graph.networkaccess.filteringPolicyLink",
            "id": "d00cf227-8645-4ab8-bd99-a9b455fd83a3",
            "state": "enabled",
            "version": "1.0.0",
            "priority": 100,
            "action": "block",
            "loggingState": "enabled",
            "lastModifiedDateTime": "2023-08-14T15:18:40Z",
            "createdDateTime": "2023-08-14T15:18:40Z",
            "policy": {
                "@odata.type": "#microsoft.graph.networkaccess.filteringPolicy",
                "id": "edfd1fa6-8080-4ac6-9858-45b13693b533",
                "name": "Social Media Sites",
                "description": null,
                "version": "1.0.0",
                "lastModifiedDateTime": "2023-08-14T15:18:06Z",
                "createdDateTime": "2023-08-14T15:18:06Z"
            }
        }
    ]
}
```

