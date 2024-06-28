---
title: "Get companySubscription"
description: "Get a specific commercial subscription that an organization acquired."
ms.localizationpriority: medium
author: "arp19690"
ms.subservice: "entra-directory-management"
doc_type: apiPageType
---

# Get companySubscription

Namespace: microsoft.graph

Get a specific commercial subscription that an organization acquired.

[!INCLUDE [national-cloud-support](../../includes/all-clouds.md)]

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- { "blockType": "permissions", "name": "companysubscription_get" } -->

[!INCLUDE [permissions-table](../includes/permissions/companysubscription-get-permissions.md)]

## HTTP request

<!-- { "blockType": "ignored" } -->

```http
GET /directory/subscriptions/{id}
GET /directory/subscriptions(commerceSubscriptionId='{commerceSubscriptionId}')
```

## Optional query parameters

This method supports the `$select` [OData query parameter](/graph/query-parameters) to help customize the response.

## Request headers

| Name          | Description                                                                                               |
| :------------ | :-------------------------------------------------------------------------------------------------------- |
| Authorization | Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts). |

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [companySubscription](../resources/companysubscription.md) object in the response body.

## Example

### Request

The following example shows a request.

<!-- {
  "blockType": "request",
  "name": "get_companySubscription"
}-->

```msgraph-interactive
GET https://graph.microsoft.com/v1.0/directory/subscriptions/f9c1ea2d-2c6e-4717-8c3b-7130812d70ba
```

---

### Response

The following example shows the response.

> **Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.companySubscription"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 450

{
  "createdDateTime": "2023-01-01T00:00:00Z",
  "commerceSubscriptionId": "f9c1ea2d-2c6e-4717-8c3b-7130812d70ba",
  "id": "860697e3-b0aa-4196-a6c6-7ec361ed58f7",
  "isTrial": false,
  "nextLifecycleDateTime": "2023-02-01T00:00:00Z",
  "serviceStatus": [
    {
      "appliesTo": "User",
      "provisioningStatus": "Success",
      "servicePlanId": "8b8269e5-f841-416c-ab3a-f5dfb9737986",
      "servicePlanName": "MyPlanName"
    }
  ],
  "skuId": "0816ccb9-3785-4d19-bf78-6c53e2106509",
  "skuPartNumber": "MyPartNumber",
  "status": "Enabled",
  "totalLicenses": 25,
  "ownerId": "fe04f19f-d924-42b7-9dee-edf4e3fab7f6",
  "ownerTenantId": "331af819-4e0b-49f7-a6bf-14e1165ad3a0",
  "ownerType": "User"
}
```
