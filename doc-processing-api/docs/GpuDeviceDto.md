# GpuDeviceDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**index** | **number** | GPU device index | [default to undefined]
**name** | **string** | GPU device name | [default to undefined]
**memoryTotalMB** | **number** | Total GPU memory in MB | [default to undefined]
**memoryUsedMB** | **number** | Used GPU memory in MB | [optional] [default to undefined]
**utilizationPct** | **number** | GPU utilization percentage | [optional] [default to undefined]

## Example

```typescript
import { GpuDeviceDto } from '@nestbox-ai/doc-processing-api';

const instance: GpuDeviceDto = {
    index,
    name,
    memoryTotalMB,
    memoryUsedMB,
    utilizationPct,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
