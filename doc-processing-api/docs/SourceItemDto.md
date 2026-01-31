# SourceItemDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Source ID | [default to undefined]
**documentId** | **string** | Associated document ID | [default to undefined]
**jobId** | **string** | Associated job ID | [optional] [default to undefined]
**chunkId** | **string** | Chunk ID | [optional] [default to undefined]
**page** | **number** | Page number | [optional] [default to undefined]
**text** | **string** | Source text content | [default to undefined]
**metadata** | **{ [key: string]: any; }** | Additional metadata | [optional] [default to undefined]

## Example

```typescript
import { SourceItemDto } from '@nestbox-ai/doc-processing-api';

const instance: SourceItemDto = {
    id,
    documentId,
    jobId,
    chunkId,
    page,
    text,
    metadata,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
