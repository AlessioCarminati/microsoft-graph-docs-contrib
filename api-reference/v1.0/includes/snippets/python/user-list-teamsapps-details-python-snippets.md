---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

from msgraph import GraphServiceClient
from msgraph.generated.users.item.teamwork.installed_apps.installed_apps_request_builder import InstalledAppsRequestBuilder

graph_client = GraphServiceClient(credentials, scopes)

query_params = InstalledAppsRequestBuilder.InstalledAppsRequestBuilderGetQueryParameters(
		expand = ["teamsAppDefinition"],
)

request_configuration = InstalledAppsRequestBuilder.InstalledAppsRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.users.by_user_id('user-id').teamwork.installed_apps.get(request_configuration = request_configuration)


```