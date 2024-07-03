---
title: "Overview"
description: "Use the Microsoft Entra scenario health monitoring API to view anomalous usage pattern for your tenant on business-critical identity scenarios and receive alert notification"
author: "huatang92"
ms.localizationpriority: medium
ms.subservice: "entra-monitoring-health"
doc_type: resourcePageType
---

# Overview

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Use the Microsoft Entra scenario health monitoring API to view anomalous usage pattern for your tenant on business-critical identity scenarios and receive alert notification

## Licenses
**TODO: Are we required user to have specific licenses?**

## Common requests

The following table lists some common requests that you can use with this API.

|  Scenarios  | API |
| ----------- | ----------- |
| Retrieve all alerts of a Microsoft Entra tenant | [List alerts](../api/healthmonitoring-healthmonitoringroot-list-alerts.md) |
| Retrieve an alert and its associated data, including the impacted resources | [Get alert](../api/healthmonitoring-alert-get.md) |
| Update an alert | [Update alert](../api/healthmonitoring-alert-update.md) |
| Retrieve alert configurations for all alert types | [List alert configurations](../api/healthmonitoring-healthmonitoringroot-list-alertconfigurations.md) |
| Retrieve alert configuration for an alert type | [Get alert configuration](../api/healthmonitoring-alertconfiguration-get.md) |
| Update alert configuration for an alert type | [Update alert configuration](../api/healthmonitoring-alertconfiguration-update.md) |
> [!NOTE]
> You may see `unknownFutureValue` as a member in enums due to evolvable enumerations, here's how you can do to [handle future members in evolvable enumerations](/graph/best-practices-concept#handling-future-members-in-evolvable-enumerations)

## Related content

* [What is Microsoft Entra Health?](/entra/identity/monitoring-health/concept-microsoft-entra-health)
* [ServiceActivity API documentation for retrieving the health metric streams upon which alerting is built](../resources/serviceactivity.md)
