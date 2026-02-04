# HealthCheckItemDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | Health check status | [default to undefined]
**latencyMs** | **number** | Latency in milliseconds | [optional] [default to undefined]
**message** | **string** | Status message | [optional] [default to undefined]
**details** | **{ [key: string]: any; }** | Additional details | [optional] [default to undefined]

## Example

```typescript
import { HealthCheckItemDto } from '@nestbox-ai/doc-processing-api';

const instance: HealthCheckItemDto = {
    status,
    latencyMs,
    message,
    details,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
