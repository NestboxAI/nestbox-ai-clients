# AdHocCallbackDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | URL to send the callback to | [default to undefined]
**eventTypes** | **Array&lt;string&gt;** | List of event types to subscribe to, such as QUERY_FAILED, QUERY_COMPLETED, etc. | [default to undefined]

## Example

```typescript
import { AdHocCallbackDto } from '@nestbox-ai/agents';

const instance: AdHocCallbackDto = {
    url,
    eventTypes,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
