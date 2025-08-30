# MachineStatusDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **string** | Current status of the machine instance | [default to undefined]
**logs** | **string** | Logs from the machine instance execution | [default to undefined]
**timeStamp** | **string** | Timestamp of the status update | [default to undefined]

## Example

```typescript
import { MachineStatusDto } from '@nestbox-ai/admin';

const instance: MachineStatusDto = {
    status,
    logs,
    timeStamp,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
