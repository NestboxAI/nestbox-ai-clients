# ProfilesApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**profilesControllerCreateProfile**](#profilescontrollercreateprofile) | **POST** /profiles | Create profile from YAML|
|[**profilesControllerGetProfile**](#profilescontrollergetprofile) | **GET** /profiles/{profileId} | Read profile|
|[**profilesControllerGetProfileSchema**](#profilescontrollergetprofileschema) | **GET** /profiles/schema | Get profile schema|
|[**profilesControllerListProfiles**](#profilescontrollerlistprofiles) | **GET** /profiles | List profiles|

# **profilesControllerCreateProfile**
> ProfileDto profilesControllerCreateProfile()

Upload a YAML config file (multipart form). Do not inline YAML parameters in JSON.

### Example

```typescript
import {
    ProfilesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new ProfilesApi(configuration);

let yaml: File; //YAML file containing the profile/config. (default to undefined)
let name: string; //Optional override for profile name (otherwise derived from YAML). (optional) (default to undefined)
let tags: Array<string>; //Optional tags to associate with the profile (e.g., [\\\"production\\\", \\\"finance\\\"]). (optional) (default to undefined)

const { status, data } = await apiInstance.profilesControllerCreateProfile(
    yaml,
    name,
    tags
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **yaml** | [**File**] | YAML file containing the profile/config. | defaults to undefined|
| **name** | [**string**] | Optional override for profile name (otherwise derived from YAML). | (optional) defaults to undefined|
| **tags** | **Array&lt;string&gt;** | Optional tags to associate with the profile (e.g., [\\\&quot;production\\\&quot;, \\\&quot;finance\\\&quot;]). | (optional) defaults to undefined|


### Return type

**ProfileDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Profile created |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |
|**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profilesControllerGetProfile**
> ProfileDto profilesControllerGetProfile()


### Example

```typescript
import {
    ProfilesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new ProfilesApi(configuration);

let profileId: string; //Profile/config ID. (default to undefined)

const { status, data } = await apiInstance.profilesControllerGetProfile(
    profileId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileId** | [**string**] | Profile/config ID. | defaults to undefined|


### Return type

**ProfileDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Profile details |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profilesControllerGetProfileSchema**
> { [key: string]: any; } profilesControllerGetProfileSchema()

Returns the JSON schema for profile YAML configuration files.

### Example

```typescript
import {
    ProfilesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new ProfilesApi(configuration);

const { status, data } = await apiInstance.profilesControllerGetProfileSchema();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**{ [key: string]: any; }**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Profile schema in JSON format |  -  |
|**401** | Unauthorized |  -  |
|**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **profilesControllerListProfiles**
> PaginatedProfilesDto profilesControllerListProfiles()


### Example

```typescript
import {
    ProfilesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new ProfilesApi(configuration);

let page: number; //1-based page number. (optional) (default to 1)
let limit: number; //Page size. (optional) (default to 10)
let tags: Array<string>; //Filter profiles by tags (any match). Pass multiple times or comma-separated. (optional) (default to undefined)

const { status, data } = await apiInstance.profilesControllerListProfiles(
    page,
    limit,
    tags
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | 1-based page number. | (optional) defaults to 1|
| **limit** | [**number**] | Page size. | (optional) defaults to 10|
| **tags** | **Array&lt;string&gt;** | Filter profiles by tags (any match). Pass multiple times or comma-separated. | (optional) defaults to undefined|


### Return type

**PaginatedProfilesDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Paginated list of profiles |  -  |
|**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

