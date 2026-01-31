# PaginatedDocumentsDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**Array&lt;DocumentDto&gt;**](DocumentDto.md) | Document data | [default to undefined]
**pagination** | [**PaginationDto**](PaginationDto.md) | Pagination information | [default to undefined]

## Example

```typescript
import { PaginatedDocumentsDto } from '@nestbox-ai/doc-processing-api';

const instance: PaginatedDocumentsDto = {
    data,
    pagination,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
