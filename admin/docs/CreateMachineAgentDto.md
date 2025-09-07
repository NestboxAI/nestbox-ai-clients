# CreateMachineAgentDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agentName** | **string** |  | [default to undefined]
**goal** | **string** |  | [default to undefined]
**modelBaseId** | **string** |  | [default to undefined]
**machineName** | **string** |  | [default to undefined]
**machineInstanceId** | **number** |  | [default to undefined]
**instanceIP** | **string** |  | [default to undefined]
**entryFunctionName** | **string** |  | [default to undefined]
**machineManifestId** | **string** |  | [default to undefined]
**type** | **string** |  | [default to undefined]
**projectId** | **string** |  | [default to undefined]
**userId** | **number** |  | [default to undefined]
**inputSchema** | **object** | Optional Input Schema JSON for agent. | [optional] [default to undefined]

## Example

```typescript
import { CreateMachineAgentDto } from '@nestbox-ai/admin';

const instance: CreateMachineAgentDto = {
    agentName,
    goal,
    modelBaseId,
    machineName,
    machineInstanceId,
    instanceIP,
    entryFunctionName,
    machineManifestId,
    type,
    projectId,
    userId,
    inputSchema,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
