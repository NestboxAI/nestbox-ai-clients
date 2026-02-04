# JobStatusDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Job ID | [default to undefined]
**state** | **string** | Job state | [default to undefined]
**updatedAt** | **string** | Job last update timestamp | [default to undefined]
**progress** | **number** | 0..1 progress fraction | [optional] [default to undefined]
**stage** | **string** | Current pipeline stage | [optional] [default to undefined]
**message** | **string** | Current job message | [optional] [default to undefined]
**error** | **string** | Error message if failed | [optional] [default to undefined]

## Example

```typescript
import { JobStatusDto } from '@nestbox-ai/doc-processing-api';

const instance: JobStatusDto = {
    id,
    state,
    updatedAt,
    progress,
    stage,
    message,
    error,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
