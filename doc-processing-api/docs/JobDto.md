# JobDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Job ID | [default to undefined]
**type** | **string** | Job type | [default to undefined]
**state** | **string** | Job state | [default to undefined]
**createdAt** | **string** | Job creation timestamp | [default to undefined]
**updatedAt** | **string** | Job last update timestamp | [optional] [default to undefined]
**profileId** | **string** | Associated profile ID | [optional] [default to undefined]
**documentId** | **string** | Associated document ID | [optional] [default to undefined]
**evalId** | **string** | Associated evaluation ID | [optional] [default to undefined]
**queryId** | **string** | Associated query ID | [optional] [default to undefined]
**progress** | **number** | 0..1 progress fraction | [optional] [default to undefined]
**stage** | **string** | Current pipeline stage | [optional] [default to undefined]
**message** | **string** | Current job message | [optional] [default to undefined]
**error** | **string** | Error message if failed | [optional] [default to undefined]
**links** | [**JobLinksDto**](JobLinksDto.md) | Job-related links | [optional] [default to undefined]
**metadata** | **{ [key: string]: any; }** | Additional job metadata | [optional] [default to undefined]

## Example

```typescript
import { JobDto } from '@nestbox-ai/doc-processing-api';

const instance: JobDto = {
    id,
    type,
    state,
    createdAt,
    updatedAt,
    profileId,
    documentId,
    evalId,
    queryId,
    progress,
    stage,
    message,
    error,
    links,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
