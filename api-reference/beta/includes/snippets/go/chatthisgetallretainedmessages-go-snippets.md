---
description: "Automatically generated file. DO NOT MODIFY"
---

```go


import (
	  "context"
	  msgraphsdk "github.com/microsoftgraph/msgraph-beta-sdk-go"
	  //other-imports
)

graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)



getAllRetainedMessages, err := graphClient.Users().ByUserId("user-id").Chats().GetAllRetainedMessages().GetAsGetAllRetainedMessagesGetResponse(context.Background(), nil)


```