# CreateWebhookDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The URL for the webhook | [default to undefined]
**notifications** | **string** | Comma-separated notifications. Valid values: QUERY_CREATED, QUERY_COMPLETED, QUERY_FAILED, EVENT_CREATED, EVENT_UPDATED | [default to undefined]

## Example

```typescript
import { CreateWebhookDto } from '@nestbox-ai/agents';

const instance: CreateWebhookDto = {
    url,
    notifications,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
