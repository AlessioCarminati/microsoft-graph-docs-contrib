---
title: "Create certificateBasedAuthPki"
description: "Create a new certificateBasedAuthPki object."
author: "suawat"
ms.localizationpriority: medium
ms.subservice: "entra-sign-in"
doc_type: apiPageType
---

# Create certificateBasedAuthPki

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new [certificateBasedAuthPki](../resources/certificatebasedauthpki.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "publickeyinfrastructureroot-post-certificatebasedauthconfigurations-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/publickeyinfrastructureroot-post-certificatebasedauthconfigurations-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /directory/publicKeyInfrastructure/certificateBasedAuthConfigurations
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|
|Content-Type|application/json. Required.|

## Request body

In the request body, supply a JSON representation of the [certificateBasedAuthPki](../resources/certificatebasedauthpki.md) object.

You can specify the following properties when creating a **certificateBasedAuthPki**.

|Property|Type|Description|
|:---|:---|:---|
|deletedDateTime|DateTimeOffset| The date time when the object was soft deleted. Inherited from base class and `null` for objects that are not deleted. Inherited from [directoryObject](../resources/directoryobject.md). Optional.|
|displayName|String|The name of the certificateBasedAuthPki object. Optional.|
|status|String|The status of any asynchronous jobs run on the certificateBasedAuthPki entity which can be upload or delete. Optional.|
|statusDetails|String|The status details of the upload/deleted operation of PKI(Public Key Infrastructure). Optional.|
|lastModifiedDateTime|DateTimeOffset|The date and time when certificateBasedAuthPki object was created or last modified. Required.|



## Response

If successful, this method returns a `201 Created` response code and a [certificateBasedAuthPki](../resources/certificatebasedauthpki.md) object in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "create_certificatebasedauthpki_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/directory/publicKeyInfrastructure/certificateBasedAuthConfigurations
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.certificateBasedAuthPki",
  "deletedDateTime": "String (timestamp)",
  "displayName": "String",
  "status": "String",
  "statusDetails": "String"
}
```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.certificateBasedAuthPki"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.certificateBasedAuthPki",
  "id": "fdd9841c-90c6-4234-a116-d72a5cd2c583",
  "deletedDateTime": null,
  "displayName": "Contoso PKI",
  "status": "succeeded",
  "statusDetails": "String",
  "lastModifiedDateTime": "String (timestamp)"
}
```