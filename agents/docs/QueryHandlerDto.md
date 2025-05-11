# QueryHandlerDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**params** | **object** | Parameters for the query, must include temperature, top_p, and max_tokens | [default to undefined]
**messages** | [**Array&lt;MessageDto&gt;**](MessageDto.md) | Messages to send to the agent | [optional] [default to undefined]

## Example

```typescript
import { QueryHandlerDto } from '@nestbox-ai/agents';

const instance: QueryHandlerDto = {
    params,
    messages,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
