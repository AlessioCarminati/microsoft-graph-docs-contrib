---
title: "subjectAlternativeNameType enum type"
description: "Subject Alternative Name Options."
author: "jaiprakashmb"
ms.localizationpriority: medium
ms.subservice: "intune"
doc_type: enumPageType
ms.date: 08/01/2024
---

# subjectAlternativeNameType enum type

Namespace: microsoft.graph
> **Important:** Microsoft Graph APIs under the /beta version are subject to change; production use is not supported.

> **Note:** The Microsoft Graph API for Intune requires an [active Intune license](https://go.microsoft.com/fwlink/?linkid=839381) for the tenant.


Subject Alternative Name Options.

## Members
|Member|Value|Description|
|:---|:---|:---|
|none|0|No subject alternative name.|
|emailAddress|1|Email address.|
|userPrincipalName|2|User Principal Name (UPN).|
|customAzureADAttribute|4|Custom Azure AD Attribute.|
|domainNameService|8|Domain Name Service (DNS).|
|universalResourceIdentifier|16|Universal Resource Identifier (URI).|
