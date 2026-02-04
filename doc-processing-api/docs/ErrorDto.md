# ErrorDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **string** | Error type | [default to undefined]
**message** | **string** | Error message | [default to undefined]
**requestId** | **string** | Request ID for tracking | [optional] [default to undefined]
**details** | **{ [key: string]: any; }** | Additional error details | [optional] [default to undefined]

## Example

```typescript
import { ErrorDto } from '@nestbox-ai/doc-processing-api';

const instance: ErrorDto = {
    error,
    message,
    requestId,
    details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
