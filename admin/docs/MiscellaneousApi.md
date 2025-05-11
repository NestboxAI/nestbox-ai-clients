# MiscellaneousApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**miscellaneousControllerGetData**](#miscellaneouscontrollergetdata) | **GET** /projects/machine/images | Get machine id matching instances.|
|[**miscellaneousControllerGetMachineInstanceByImageId**](#miscellaneouscontrollergetmachineinstancebyimageid) | **GET** /projects/{projectId}/allMachineInstance | Get machine id matching instances.|
|[**miscellaneousControllerUpdateTeamMemberStatus**](#miscellaneouscontrollerupdateteammemberstatus) | **PATCH** /projects/member/join | Join project|

# **miscellaneousControllerGetData**
> object miscellaneousControllerGetData()


### Example

```typescript
import {
    MiscellaneousApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MiscellaneousApi(configuration);

const { status, data } = await apiInstance.miscellaneousControllerGetData();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **miscellaneousControllerGetMachineInstanceByImageId**
> object miscellaneousControllerGetMachineInstanceByImageId()


### Example

```typescript
import {
    MiscellaneousApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MiscellaneousApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.miscellaneousControllerGetMachineInstanceByImageId(
    projectId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|


### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **miscellaneousControllerUpdateTeamMemberStatus**
> AddProjectMemberResponseDTO miscellaneousControllerUpdateTeamMemberStatus(updateTeamMemberStatusRequestDTO)


### Example

```typescript
import {
    MiscellaneousApi,
    Configuration,
    UpdateTeamMemberStatusRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MiscellaneousApi(configuration);

let updateTeamMemberStatusRequestDTO: UpdateTeamMemberStatusRequestDTO; //

const { status, data } = await apiInstance.miscellaneousControllerUpdateTeamMemberStatus(
    updateTeamMemberStatusRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateTeamMemberStatusRequestDTO** | **UpdateTeamMemberStatusRequestDTO**|  | |


### Return type

**AddProjectMemberResponseDTO**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |
|**400** |  |  -  |
|**401** |  |  -  |
|**403** |  |  -  |
|**404** |  |  -  |
|**500** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

