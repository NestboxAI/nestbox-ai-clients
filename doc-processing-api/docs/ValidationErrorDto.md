# ValidationErrorDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **string** | Error type | [default to undefined]
**message** | **string** | Error message | [default to undefined]
**issues** | [**Array&lt;ValidationIssueDto&gt;**](ValidationIssueDto.md) | Validation issues | [default to undefined]
**requestId** | **string** | Request ID for tracking | [optional] [default to undefined]

## Example

```typescript
import { ValidationErrorDto } from '@nestbox-ai/doc-processing-api';

const instance: ValidationErrorDto = {
    error,
    message,
    issues,
    requestId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
