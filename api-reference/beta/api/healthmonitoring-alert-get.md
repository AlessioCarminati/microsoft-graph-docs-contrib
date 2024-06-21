---
title: "Get alert"
description: "Read the properties and relationships of a microsoft.graph.healthMonitoring.alert object."
author: "huatang92"
ms.localizationpriority: medium
ms.subservice: "entra-monitoring-health"
doc_type: apiPageType
---

# Get alert

Namespace: microsoft.graph.healthMonitoring

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [microsoft.graph.healthMonitoring.alert](../resources/healthmonitoring-alert.md) object.

## Permissions

Choose the permission or permissions marked as least privileged for this API. Use a higher privileged permission or permissions [only if your app requires it](/graph/permissions-overview#best-practices-for-using-microsoft-graph-permissions). For details about delegated and application permissions, see [Permission types](/graph/permissions-overview#permission-types). To learn more about these permissions, see the [permissions reference](/graph/permissions-reference).

<!-- {
  "blockType": "permissions",
  "name": "healthmonitoring-alert-get-permissions"
}
-->
[!INCLUDE [permissions-table](../includes/permissions/healthmonitoring-alert-get-permissions.md)]

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/healthMonitoring/alerts/{alertId}
```

## Optional query parameters

This method supports the `$select` and `$expand` [OData query parameters](/graph/query-parameters) to help customize the response.

When no `$expand` query parameter is added, this API doesn't return `resourceSampling` property by default. When you want to retrieve a sample of the resources involved in triggering the alert for root cause investigation, you can add `$expand=enrichment/impacts/microsoft.graph.healthmonitoring.directoryobjectimpactsummary/resourceSampling` to view `resourceSampling` in [directoryObjectImpactSummary](../resources//healthmonitoring-directoryobjectimpactsummary.md).

## Request headers

|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required. Learn more about [authentication and authorization](/graph/auth/auth-concepts).|

## Request body

Don't supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [microsoft.graph.healthMonitoring.alert](../resources/healthmonitoring-alert.md) object in the response body.

## Examples

### Example 1: Get the properties of the specified alert

#### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_alert"
}
-->
``` http
GET https://graph.microsoft.com/beta/reports/healthMonitoring/alerts/{id}
```

#### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.healthMonitoring.alert)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#reports/healthMonitoring/alerts/$entity",
  "id": "0c56dfcb-13db-4128-bda2-fc3e42742467",
  "alertType": "mfaSignInFailure",
  "scenario": "mfa",
  "category": "authentication",
  "createdDateTime": "2024-06-19T11:23:44.1234567Z",
  "state": "active",
  "enrichment": {
    "state": "enriched",
    "impacts": [
      {
        "@odata.type": "#microsoft.graph.healthMonitoring.userImpactSummary",
        "resourceType": "user",
        "impactedCount": 143,
        "impactedCountLimitExceeded": false
      },
      {
        "@odata.type": "#microsoft.graph.healthMonitoring.applicationImpactSummary",
        "resourceType": "application",
        "impactedCount": 1,
        "impactedCountLimitExceeded": true
      }
    ],
    "supportingData": {
      "signInRecords": "https://graph.microsoft.com/beta/auditLogs/signIns?$filter=({errorCodeFilterStr} and createdDateTime gt {startTime} and createdDateTime le {endTime} and (signInEventTypes/any(t:t eq 'interactiveUser' or t eq 'noninteractiveUser')))",
      "auditRecords": "https://graph.microsoft.com/beta/auditLogs/directoryaudits?$filter=(activityDateTime ge {startTime} and activityDateTime le {endTime})&$top=50&$orderby=activityDateTime desc"
    }
  },
  "signals": {
    "mfaSignInFailure": "https://graph.microsoft.com/beta/reports/serviceActivity/getMetricsForMfaSignInFailure(inclusiveIntervalStartDateTime={startTime}, exclusiveIntervalEndDateTime={endTime}, aggregationIntervalInMinutes=5)"
  },
  "documentation": {
    "mfaAlertTroubleshootingGuide": "https://learn.microsoft.com/en-us/entra/identity/authentication/"
  }
}
```

### Example 2: Use $select to retrieve specific properties of an alert

#### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_alert"
}
-->
``` http
GET https://graph.microsoft.com/beta/reports/healthMonitoring/alerts/{id}?$select=alertType, state, createdDateTime, signals
```

#### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.healthMonitoring.alert)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#reports/healthMonitoring/alerts(alertType,state,createdDateTime,signals)/$entity",
  "alertType": "mfaSignInFailure",
  "createdDateTime": "2024-06-19T11:23:44.1234567Z",
  "state": "active",
  "signals": {
    "mfaSignInFailure": "https://graph.microsoft.com/beta/reports/serviceActivity/getMetricsForMfaSignInFailure(inclusiveIntervalStartDateTime={startTime}, exclusiveIntervalEndDateTime={endTime}, aggregationIntervalInMinutes=5)"
  }
}
```

### Example 3: Use $expand to show resource sampling of an alert

#### Request

The following example shows a request.
<!-- {
  "blockType": "request",
  "name": "list_alert"
}
-->
``` http
GET https://graph.microsoft.com/beta/reports/healthMonitoring/alerts/{id}?$expand=enrichment/impacts/microsoft.graph.healthmonitoring.directoryobjectimpactsummary/resourceSampling&$select=alertType, createdDateTime, enrichment'
```

#### Response

The following example shows the response.
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.healthMonitoring.alert)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#reports/healthMonitoring/alerts/$entity",
  "alertType": "mfaSignInFailure",
  "createdDateTime": "2024-06-19T11:23:44.1234567Z",
  "enrichment": {
    "state": "enriched",
    "impacts": [
      {
        "@odata.type": "#microsoft.graph.healthMonitoring.userImpactSummary",
        "resourceType": "user",
        "impactedCount": 143,
        "impactedCountLimitExceeded": false,
        "resourceSampling": []
      },
      {
        "@odata.type": "#microsoft.graph.healthMonitoring.applicationImpactSummary",
        "resourceType": "application",
        "impactedCount": 1,
        "impactedCountLimitExceeded": true,
        "resourceSampling": [
          {
              "id": "63c83fa4-d90c-4274-8460-5463e96f1113"
          }
        ]
      }
    ],
    "supportingData": {
      "signInRecords": "https://graph.microsoft.com/beta/auditLogs/signIns?$filter=({errorCodeFilterStr} and createdDateTime gt {startTime} and createdDateTime le {endTime} and (signInEventTypes/any(t:t eq 'interactiveUser' or t eq 'noninteractiveUser')))",
      "auditRecords": "https://graph.microsoft.com/beta/auditLogs/directoryaudits?$filter=(activityDateTime ge {startTime} and activityDateTime le {endTime})&$top=50&$orderby=activityDateTime desc"
    }
  }
}
```

> Note: Currently `resourceSampling` only contains `id` of the resource. In the future, it'll be able to show other properties of the resource as well.
