---
title: "Remove application"
description: "Remove an application object."
author: "**TODO: Provide GitHub Name. See [topic-level metadata reference](https://aka.ms/msgo?pagePath=Document-APIs/Guidelines/Metadata)**"
ms.localizationpriority: medium
ms.subservice: "**TODO: Add MS subservice. See [topic-level metadata reference](https://aka.ms/msgo?pagePath=Document-APIs/Guidelines/Metadata)**"
doc_type: apiPageType
---

# Remove application

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Remove an [application](../resources/application.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "ipapplicationsegment-delete-application-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/ipapplicationsegment-delete-application-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /onPremisesPublishingProfiles/{onPremisesPublishingProfilesId}/applicationSegments/{ipApplicationSegmentId}/application/{id}/$ref
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `204 No Content` response code.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "delete_application_from_ipapplicationsegment"
}
-->
``` http
DELETE https://graph.microsoft.com/beta/onPremisesPublishingProfiles/{onPremisesPublishingProfilesId}/applicationSegments/{ipApplicationSegmentId}/application/{id}/$ref
```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```

