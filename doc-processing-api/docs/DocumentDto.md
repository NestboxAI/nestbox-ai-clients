# DocumentDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Document ID | [default to undefined]
**profileId** | **string** | Associated profile ID | [default to undefined]
**status** | **string** | Document processing status | [default to undefined]
**fileName** | **string** | Original file name | [optional] [default to undefined]
**contentType** | **string** | MIME content type | [optional] [default to undefined]
**sizeBytes** | **number** | File size in bytes | [optional] [default to undefined]
**createdAt** | **string** | Document creation timestamp | [default to undefined]
**updatedAt** | **string** | Document last update timestamp | [optional] [default to undefined]
**latestJobId** | **string** | Latest job ID associated with this document | [optional] [default to undefined]
**metrics** | **{ [key: string]: any; }** | Optional processing metrics (pages, chunks, entities, etc.) | [optional] [default to undefined]
**tags** | **Array&lt;string&gt;** | Tags associated with the document | [optional] [default to undefined]

## Example

```typescript
import { DocumentDto } from '@nestbox-ai/doc-processing-api';

const instance: DocumentDto = {
    id,
    profileId,
    status,
    fileName,
    contentType,
    sizeBytes,
    createdAt,
    updatedAt,
    latestJobId,
    metrics,
    tags,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
