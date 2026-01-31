# HealthResponseDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | Overall system health status | [default to undefined]
**timestamp** | **string** | Health check timestamp | [default to undefined]
**checks** | [**HealthChecksDto**](HealthChecksDto.md) | Health check results | [default to undefined]

## Example

```typescript
import { HealthResponseDto } from '@nestbox-ai/doc-processing-api';

const instance: HealthResponseDto = {
    status,
    timestamp,
    checks,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
