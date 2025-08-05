# CreateRoleDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** |  | [default to undefined]
**description** | **string** |  | [default to undefined]
**resources** | [**Array&lt;CreateResourceDto&gt;**](CreateResourceDto.md) |  | [default to undefined]

## Example

```typescript
import { CreateRoleDto } from '@nestbox-ai/admin';

const instance: CreateRoleDto = {
    name,
    description,
    resources,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
