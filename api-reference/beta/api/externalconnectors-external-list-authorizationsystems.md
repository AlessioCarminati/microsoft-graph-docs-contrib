---
title: "List authorizationSystems"
description: "List the authorizationSystem objects and their properties."
author: "mrudulahg01"
ms.reviewer: ciem_pm
ms.localizationpriority: medium
ms.prod: "multicloud-permissions-management"
doc_type: apiPageType
---

# List authorizationSystems
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

List the [authorizationSystem](../resources/authorizationsystem.md) objects onboarded to Permissions Management and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Not supported.|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

<!--
[!INCLUDE [epm-rbac-servicenow-apis-read](../includes/rbac-for-apis/epm-rbac-servicenow-apis-read.md)]
-->

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /external/authorizationSystems
```

## Optional query parameters
This method supports the `$filter`, `$orderby`, and `$skip` OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [authorizationSystem](../resources/authorizationsystem.md) objects in the response body.

## Examples

### Example 1: List authorization systems onboarded to Permissions Management

#### Request
The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_authorizationsystem"
}
-->
``` http
GET https://graph.microsoft.com/beta/external/authorizationSystems
```


#### Response
The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.authorizationSystem)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#external/authorizationSystems",
  "value": [
    {
      "@odata.type": "#microsoft.graph.awsAuthorizationSystem",
      "id": "Mzc3NTk2MTMxNzc0",
      "authorizationSystemId": "377596131774",
      "authorizationSystemName": "staging",
      "authorizationSystemType": "AWS",
      "dataCollectionInfo@odata.context": "https://graph.microsoft.com/beta/$metadata#external/authorizationSystems('Mzc3NTk2MTMxNzc0')/microsoft.graph.awsAuthorizationSystem/dataCollectionInfo/$entity",
      "dataCollectionInfo": {
        "entitlements": {
          "@odata.type": "microsoft.graph.entitlementsDataCollection",
          "status": "offline",
          "lastCollectionDateTime": "2023-02-17T21:12:48Z",
          "permissionsModificationCapability":  "enabled"
        }
      }
    },
    {
      "@odata.type": "#microsoft.graph.awsAuthorizationSystem",
      "id": "OTU2OTg3ODg3NzM1",
      "authorizationSystemId": "956987887735",
      "authorizationSystemName": "development",
      "authorizationSystemType": "AWS",
      "dataCollectionInfo@odata.context": "https://graph.microsoft.com/beta/$metadata#external/authorizationSystems('OTU2OTg3ODg3NzM1')/microsoft.graph.awsAuthorizationSystem/dataCollectionInfo/$entity",
      "dataCollectionInfo": {
        "entitlements": {
          "@odata.type": "microsoft.graph.noEntitlementsDataCollection"
        }
      }
    },
    {
      "@odata.type": "#microsoft.graph.azureAuthorizationSystem",
      "id": "NTc1N2Y5NzAtYTcwMS00YTJkLThjZGItOTdjODU4MjE2MDg0",
      "authorizationSystemId": "5757f970-a701-4a2d-8cdb-97c858216084",
      "authorizationSystemName": "Microsoft Azure Sponsorship 2",
      "authorizationSystemType": "AZURE",
      "dataCollectionInfo@odata.context": "https://graph.microsoft.com/beta/$metadata#external/authorizationSystems('NTc1N2Y5NzAtYTcwMS00YTJkLThjZGItOTdjODU4MjE2MDg0')/microsoft.graph.azureAuthorizationSystem/dataCollectionInfo/$entity",
      "dataCollectionInfo": {
        "entitlements": {
          "@odata.type": "microsoft.graph.entitlementsDataCollection",
          "status": "online",
          "lastCollectionDateTime": "2023-03-17T21:12:48Z",
          "permissionsModificationCapability": "notConfigured"
        }
      }
    },
    {
      "@odata.type": "#microsoft.graph.gcpAuthorizationSystem",
      "id": "Y2FyYmlkZS1ib25zYWktMjA1MDE3",
      "authorizationSystemId": "carbide-bonsai-205017",
      "authorizationSystemName": "ck-staging",
      "authorizationSystemType": "GCP",
      "dataCollectionInfo@odata.context": "https://canary.graph.microsoft.com/beta/$metadata#external/authorizationSystems('Y2FyYmlkZS1ib25zYWktMjA1MDE3')/microsoft.graph.gcpAuthorizationSystem/dataCollectionInfo/$entity",
      "dataCollectionInfo": {
        "entitlements": {
          "@odata.type": "microsoft.graph.entitlementsDataCollection",
          "status": "offline",
          "lastCollectionDateTime": "2023-02-17T21:12:48Z",
          "permissionsModificationCapability":  "noRecentDataCollected"
        }
      }
    }
  ],
  "@odata.nextLink": "https://graph.microsoft.com/beta/external/authorizationSystems?$skiptoken=MQ",
}
```

### Example 2: Identify all the authorization systems that are online and have permissions modification capability enabled

#### Request
The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_authorizationsystem_filter"
}
-->
``` http
GET https://graph.microsoft.com/beta/external/authorizationSystems?$filter=dataCollectionInfo/entitlements/microsoft.graph.entitlementsDataCollection/permissionsModificationCapability eq 'enabled' and dataCollectionInfo/entitlements/microsoft.graph.entitlementsDataCollection/status eq 'online'
```


#### Response
The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.authorizationSystem)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{  
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#external/authorizationSystems/$entity",  
  "value": [  
    {  
      "@odata.type": "#microsoft.graph.awsAuthorizationSystem",  
      "id": "OTU2OTg3ODg3NzM1",  
      "authorizationSystemId": "956987887735",  
      "authorizationSystemName": "development",  
      "authorizationSystemType": "AWS",  
      "dataCollectionInfo@odata.context": "https://graph.microsoft.com/beta/$metadata#external/authorizationSystems('OTU2OTg3ODg3NzM1')/microsoft.graph.awsAuthorizationSystem/dataCollectionInfo/$entity",  
      "dataCollectionInfo": {  
        "entitlements": {  
          "@odata.type": "microsoft.graph.entitlementsDataCollection",  
          "status": "online",  
          "lastCollectionDateTime": "2023-02-17T21:12:48Z",  
          "permissionsModificationCapability": "enabled"  
        }  
      }  
    },  
  ],  
  "@odata.nextLink": "https://graph.microsoft.com/beta/external/authorizationSystems?$filter=dataCollectionInfo%2fentitlements%2fmicrosoft.graph.entitlementsDataCollection%2fpermissionsModificationCapability+eq+%27enabled%27+and+dataCollectionInfo%2fentitlements%2fmicrosoft.graph.entitlementsDataCollection%2fstatus+eq+%27online%27&$skiptoken=MQ",  
}  
```
