# BatchQueryDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Batch query ID | [default to undefined]
**documentId** | **string** | Associated document ID | [optional] [default to undefined]
**status** | **string** | Batch query status | [default to undefined]
**createdAt** | **string** | Batch query creation timestamp | [default to undefined]
**updatedAt** | **string** | Batch query last update timestamp | [optional] [default to undefined]
**latestJobId** | **string** | Latest job ID associated with this batch query | [optional] [default to undefined]
**yamlFileName** | **string** | YAML file name | [optional] [default to undefined]
**results** | **{ [key: string]: any; }** | Optional stored results (if persisted) | [optional] [default to undefined]

## Example

```typescript
import { BatchQueryDto } from '@nestbox-ai/doc-processing-api';

const instance: BatchQueryDto = {
    id,
    documentId,
    status,
    createdAt,
    updatedAt,
    latestJobId,
    yamlFileName,
    results,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
