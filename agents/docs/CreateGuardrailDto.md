# CreateGuardrailDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**isActive** | **boolean** | Whether the guardrail is active | [default to undefined]
**thresholdSetting** | **number** | Threshold setting ranging from 0.0 to 1.0 | [default to undefined]
**severity** | **string** | Severity level of the guardrail | [default to undefined]
**risk** | **string** | Risk level of the guardrail | [default to undefined]
**flag** | **string** | Flag status for the guardrail | [default to undefined]
**guardrailUsers** | [**Array&lt;GuardrailUserDto&gt;**](GuardrailUserDto.md) | List of users associated with the guardrail | [optional] [default to undefined]

## Example

```typescript
import { CreateGuardrailDto } from '@nestbox-ai/agents';

const instance: CreateGuardrailDto = {
    isActive,
    thresholdSetting,
    severity,
    risk,
    flag,
    guardrailUsers,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
