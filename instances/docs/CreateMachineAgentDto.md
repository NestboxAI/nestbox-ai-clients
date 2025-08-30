# CreateMachineAgentDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**entryFunctionName** | **string** |  | [optional] [default to undefined]
**type** | **string** |  | [default to undefined]
**parameters** | [**Array&lt;AgentParameterDto&gt;**](AgentParameterDto.md) |  | [optional] [default to undefined]
**additionalParameters** | [**Array&lt;AdditionalAgentParameterDto&gt;**](AdditionalAgentParameterDto.md) |  | [optional] [default to undefined]
**machineManifestId** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { CreateMachineAgentDto } from '@nestbox-ai/instances';

const instance: CreateMachineAgentDto = {
    name,
    description,
    entryFunctionName,
    type,
    parameters,
    additionalParameters,
    machineManifestId,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
