# MembersApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**membersControllerAddTeamMemberToProject**](#memberscontrolleraddteammembertoproject) | **POST** /projects/{projectId}/members | Add a team member|
|[**membersControllerGetAllTeamMembersOfProject**](#memberscontrollergetallteammembersofproject) | **GET** /projects/{projectId}/members | Retrieve all team members|
|[**membersControllerUpdateTeamMemberRole**](#memberscontrollerupdateteammemberrole) | **PATCH** /projects/{projectId}/members/{memberId} | Update team member details|

# **membersControllerAddTeamMemberToProject**
> AddProjectMemberResponseDTO membersControllerAddTeamMemberToProject(addProjectMemberDto)


### Example

```typescript
import {
    MembersApi,
    Configuration,
    AddProjectMemberDto
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MembersApi(configuration);

let projectId: string; // (default to undefined)
let addProjectMemberDto: AddProjectMemberDto; //

const { status, data } = await apiInstance.membersControllerAddTeamMemberToProject(
    projectId,
    addProjectMemberDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **addProjectMemberDto** | **AddProjectMemberDto**|  | |
| **projectId** | [**string**] |  | defaults to undefined|


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

# **membersControllerGetAllTeamMembersOfProject**
> GetAllProjectMemberResponseDto membersControllerGetAllTeamMembersOfProject()


### Example

```typescript
import {
    MembersApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MembersApi(configuration);

let projectId: string; // (default to undefined)
let page: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)
let column: string; // (optional) (default to undefined)
let direction: 'ASC' | 'DESC'; // (optional) (default to undefined)
let teamMemberStatus: Array<string>; // (optional) (default to undefined)
let roleIds: Array<number>; // (optional) (default to undefined)

const { status, data } = await apiInstance.membersControllerGetAllTeamMembersOfProject(
    projectId,
    page,
    limit,
    column,
    direction,
    teamMemberStatus,
    roleIds
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **page** | [**number**] |  | (optional) defaults to undefined|
| **limit** | [**number**] |  | (optional) defaults to undefined|
| **column** | [**string**] |  | (optional) defaults to undefined|
| **direction** | [**&#39;ASC&#39; | &#39;DESC&#39;**]**Array<&#39;ASC&#39; &#124; &#39;DESC&#39;>** |  | (optional) defaults to undefined|
| **teamMemberStatus** | **Array&lt;string&gt;** |  | (optional) defaults to undefined|
| **roleIds** | **Array&lt;number&gt;** |  | (optional) defaults to undefined|


### Return type

**GetAllProjectMemberResponseDto**

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

# **membersControllerUpdateTeamMemberRole**
> AddProjectMemberResponseDTO membersControllerUpdateTeamMemberRole(updateTeamMemberRequestDTO)


### Example

```typescript
import {
    MembersApi,
    Configuration,
    UpdateTeamMemberRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MembersApi(configuration);

let projectId: string; // (default to undefined)
let memberId: string; // (default to undefined)
let updateTeamMemberRequestDTO: UpdateTeamMemberRequestDTO; //

const { status, data } = await apiInstance.membersControllerUpdateTeamMemberRole(
    projectId,
    memberId,
    updateTeamMemberRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateTeamMemberRequestDTO** | **UpdateTeamMemberRequestDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **memberId** | [**string**] |  | defaults to undefined|


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

