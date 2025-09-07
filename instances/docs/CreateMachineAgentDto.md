# CreateMachineAgentDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**entryFunctionName** | **string** |  | [optional] [default to undefined]
**type** | **string** |  | [default to undefined]
**machineManifestId** | **string** |  | [optional] [default to undefined]
**inputSchema** | **object** | Optional Input Schema JSON for agent. | [optional] [default to undefined]

## Example

```typescript
import { CreateMachineAgentDto } from '@nestbox-ai/instances';

const instance: CreateMachineAgentDto = {
    name,
    description,
    entryFunctionName,
    type,
    machineManifestId,
    inputSchema,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
