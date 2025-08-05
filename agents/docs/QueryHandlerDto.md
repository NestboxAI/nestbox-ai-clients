# QueryHandlerDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**params** | **object** | Parameters for the query | [default to undefined]
**messages** | [**Array&lt;MessageDto&gt;**](MessageDto.md) | Messages to send to the agent | [optional] [default to undefined]
**adHocCallback** | [**AdHocCallbackDto**](AdHocCallbackDto.md) | Ephemeral callback registration webhook | [optional] [default to undefined]

## Example

```typescript
import { QueryHandlerDto } from '@nestbox-ai/agents';

const instance: QueryHandlerDto = {
    params,
    messages,
    adHocCallback,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
