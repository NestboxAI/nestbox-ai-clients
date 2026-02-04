# GpuHealthCheckDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | GPU health status | [default to undefined]
**deviceCount** | **number** | Number of GPU devices | [optional] [default to undefined]
**devices** | [**Array&lt;GpuDeviceDto&gt;**](GpuDeviceDto.md) | GPU devices information | [optional] [default to undefined]
**message** | **string** | GPU status message | [optional] [default to undefined]

## Example

```typescript
import { GpuHealthCheckDto } from '@nestbox-ai/doc-processing-api';

const instance: GpuHealthCheckDto = {
    status,
    deviceCount,
    devices,
    message,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
