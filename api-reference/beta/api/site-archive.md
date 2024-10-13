---
title: "site: archive"
description: "Archive an active SharePoint site."
ms.localizationpriority: medium
author: neelporiya
ms.subservice: "sharepoint"
doc_type: apiPageType
---
# Archive site 

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Archive an active SharePoint [site](../resources/site.md).

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- this will be generated automatically -->

In delegated scenarios, the signed-in user must also be assigned one of the following supported [Microsoft Entra roles](/entra/identity/role-based-access-control/permissions-reference) for this operation:

* SharePoint Administrator
* Global Administrator

*SharePoint Administrator* is the least privileged role for this operation.

## HTTP request

```http
POST /sites/{site-id}/archive
```

## Request headers

| Name          | Description               |
| :------------ | :------------------------ |
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response 

If successful, this method returns a `204 No Content` response code. It doesn't return anything in the response body.

## Examples

### Request

The following example shows how to archive a site.

<!-- {
  "blockType": "request",
  "name": "archive_site"
}
-->
```http
POST https://graph.microsoft.com/beta/sites/{site-id}/archive
```

### Response

The following example shows the response.

<!-- {
  "blockType": "response",
  "truncated": true
}
-->
```http
HTTP/1.1 204 No Content
```
