# MessageDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique message ID | [default to undefined]
**role** | **string** | Role of the message sender (system, user, assistant) | [default to undefined]
**content** | **string** | Content of the message | [default to undefined]

## Example

```typescript
import { MessageDto } from '@nestbox-ai/agents';

const instance: MessageDto = {
    id,
    role,
    content,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
