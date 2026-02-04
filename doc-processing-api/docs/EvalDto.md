# EvalDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Evaluation ID | [default to undefined]
**documentId** | **string** | Associated document ID | [default to undefined]
**status** | **string** | Evaluation status | [default to undefined]
**createdAt** | **string** | Evaluation creation timestamp | [default to undefined]
**updatedAt** | **string** | Evaluation last update timestamp | [optional] [default to undefined]
**latestJobId** | **string** | Latest job ID associated with this evaluation | [optional] [default to undefined]
**yamlFileName** | **string** | YAML file name | [optional] [default to undefined]
**summary** | **{ [key: string]: any; }** | Optional aggregated metrics (e.g., similarity scores) | [optional] [default to undefined]
**report** | **{ [key: string]: any; }** | Optional detailed report (if stored) | [optional] [default to undefined]

## Example

```typescript
import { EvalDto } from '@nestbox-ai/doc-processing-api';

const instance: EvalDto = {
    id,
    documentId,
    status,
    createdAt,
    updatedAt,
    latestJobId,
    yamlFileName,
    summary,
    report,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
