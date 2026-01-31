# ProfileDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Profile ID | [default to undefined]
**name** | **string** | Profile name | [default to undefined]
**description** | **string** | Profile description | [optional] [default to undefined]
**createdAt** | **string** | Profile creation timestamp | [default to undefined]
**updatedAt** | **string** | Profile last update timestamp | [optional] [default to undefined]
**yamlFileName** | **string** | YAML file name | [optional] [default to undefined]
**yamlSha256** | **string** | Optional checksum of the uploaded YAML file | [optional] [default to undefined]

## Example

```typescript
import { ProfileDto } from '@nestbox-ai/doc-processing-api';

const instance: ProfileDto = {
    id,
    name,
    description,
    createdAt,
    updatedAt,
    yamlFileName,
    yamlSha256,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
