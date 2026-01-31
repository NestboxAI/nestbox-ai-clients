# HealthChecksDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**redis** | [**HealthCheckItemDto**](HealthCheckItemDto.md) | Redis health check | [default to undefined]
**db** | [**HealthCheckItemDto**](HealthCheckItemDto.md) | Database health check | [default to undefined]
**gpu** | [**GpuHealthCheckDto**](GpuHealthCheckDto.md) | GPU health check | [default to undefined]

## Example

```typescript
import { HealthChecksDto } from '@nestbox-ai/doc-processing-api';

const instance: HealthChecksDto = {
    redis,
    db,
    gpu,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
