# ValidationIssueDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **string** | JSON pointer-like path into the YAML document | [default to undefined]
**message** | **string** | Validation issue message | [default to undefined]
**severity** | **string** | Issue severity | [optional] [default to SeverityEnum_Error]

## Example

```typescript
import { ValidationIssueDto } from '@nestbox-ai/doc-processing-api';

const instance: ValidationIssueDto = {
    path,
    message,
    severity,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
