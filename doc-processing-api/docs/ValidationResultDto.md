# ValidationResultDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **boolean** | Whether the validation passed | [default to undefined]
**warnings** | [**Array&lt;ValidationIssueDto&gt;**](ValidationIssueDto.md) | Non-fatal issues | [optional] [default to undefined]
**normalized** | **{ [key: string]: any; }** | Optional normalized representation (if available) | [optional] [default to undefined]

## Example

```typescript
import { ValidationResultDto } from '@nestbox-ai/doc-processing-api';

const instance: ValidationResultDto = {
    valid,
    warnings,
    normalized,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
