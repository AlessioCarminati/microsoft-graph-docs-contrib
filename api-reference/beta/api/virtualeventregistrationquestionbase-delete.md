---
title: "Delete virtualEventRegistrationQuestionBase"
description: "Delete a registration question from a webinar."
author: "frankpeng7"
ms.localizationpriority: medium
ms.subservice: "cloud-communications"
doc_type: apiPageType
---

# Delete virtualEventRegistrationQuestionBase
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Delete a registration question from a [webinar](../resources/virtualeventwebinar.md). The question can either be a [predefined registration question](../resources/virtualeventregistrationpredefinedquestion.md) or a [custom registration question](../resources/virtualeventregistrationcustomquestion.md). 

[!INCLUDE [national-cloud-support](../../includes/global-only.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "virtualeventregistrationquestionbase_delete" } -->
[!INCLUDE [permissions-table](../includes/permissions/virtualeventregistrationquestionbase-delete-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /solutions/virtualEvents/webinars/{webinarId}/registrationConfiguration/questions/{questionId}
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
  "name": "delete_virtualeventregistrationquestion",
  "sampleKeys": ["f4b39f1c-520e-4e75-805a-4b0f2016a0c6@a1a56d21-a8a6-4a6b-97f8-ced53d30f143", "f3115d4c-9896-42fc-a649-8ca5e3c3a43f"]
}
-->
``` http
DELETE https://graph.microsoft.com/beta/solutions/virtualEvents/webinars/f4b39f1c-520e-4e75-805a-4b0f2016a0c6@a1a56d21-a8a6-4a6b-97f8-ced53d30f143/registrationConfiguration/questions/f3115d4c-9896-42fc-a649-8ca5e3c3a43f
```

### Response

The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 204 No Content
```
