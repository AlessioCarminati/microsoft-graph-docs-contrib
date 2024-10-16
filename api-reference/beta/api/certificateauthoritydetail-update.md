---
title: "Update certificateAuthorityDetail"
description: "Update the properties of a certificateAuthorityDetail object."
author: "suawat"
ms.localizationpriority: medium
ms.subservice: "entra-sign-in"
doc_type: apiPageType
---

# Update certificateAuthorityDetail

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [certificateAuthorityDetail](../resources/certificateauthoritydetail.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "certificateauthoritydetail-update-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/certificateauthoritydetail-update-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /directory/publicKeyInfrastructure/certificateBasedAuthConfigurations/{certificateBasedAuthPkiId}/certificateAuthorities/{certificateAuthorityDetailId}
```

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|
|Content-Type|application/json. Required.|

## Request body

[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]


|Property|Type|Description|
|:---|:---|:---|
|deletedDateTime|DateTimeOffset| The date and time when the object was soft deleted. Inherited from base class and `null` for objects that aren't deleted. Inherited from [directoryObject](../resources/directoryobject.md). Optional.|
|certificateAuthorityType|certificateAuthorityType|The type of certificate authority. The possible values are: `root`, `intermediate`, `unknownFutureValue`. Optional.|
|certificate|Binary|The type of certificate authority whether `root` or `intermediate`. Required.|
|displayName|String|The name of the certificateBasedAuthPki entity. Optional.|
|issuer|String|The name of the certificate authority. Optional.|
|issuerSubjectKeyIdentifier|String|The subject key identifier of certificate authority. Optional.|
|createdDateTime|DateTimeOffset|The creation DateTime of the certificate authority. Optional.|
|expirationDateTime|DateTimeOffset|The expirationTime of the certificate authority. Required.|
|thumbprint|String|The thumbprint of the certificate authority public certificate. Required.|
|certificateRevocationListUrl|String|The URL to check if the certificate is revoked. Optional.|
|deltacertificateRevocationListUrl|String|The URL to check if the certificate is revoked. Optional.|
|isIssuerHintEnabled|Boolean|`true` to enable the the issuer hint feature. The certificate picker presents the certificate to the user to use for authentication. `false` by default. Optional.|



## Response

If successful, this method returns a `200 OK` response code and an updated [certificateAuthorityDetail](../resources/certificateauthoritydetail.md) object in the response body.

## Examples

### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "update_certificateauthoritydetail"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/directory/publicKeyInfrastructure/certificateBasedAuthConfigurations/{certificateBasedAuthPkiId}/certificateAuthorities/{certificateAuthorityDetailId}
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.certificateAuthorityDetail",
  "deletedDateTime": "String (timestamp)",
  "certificateAuthorityType": "String",
  "certificate": "Binary",
  "displayName": "String",
  "issuer": "String",
  "issuerSubjectKeyIdentifier": "String",
  "expirationDateTime": "String (timestamp)",
  "thumbprint": "String",
  "certificateRevocationListUrl": "String",
  "deltacertificateRevocationListUrl": "String",
  "isIssuerHintEnabled": "Boolean"
}
```


### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.certificateAuthorityDetail"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.certificateAuthorityDetail",
  "id": "90777c92-2eb3-4a68-931d-4a3e1e1c741f",
  "deletedDateTime": null,
  "certificateAuthorityType": "root",
  "certificate": "Binary",
  "displayName": "Contoso2 CA1",
  "issuer": "Contoso2",
  "issuerSubjectKeyIdentifier": "String",
  "createdDateTime": null,
  "expirationDateTime": "2027-08-29T02:05:57Z",
  "thumbprint": "String",
  "certificateRevocationListUrl": null,
  "deltacertificateRevocationListUrl": null,
  "isIssuerHintEnabled": true

}
```

