# RolesApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**rolesControllerCreateProjectRole**](#rolescontrollercreateprojectrole) | **POST** /projects/{projectId}/roles | Create a new role|
|[**rolesControllerDeleteProjectRole**](#rolescontrollerdeleteprojectrole) | **DELETE** /projects/{projectId}/roles/{roleId} | Delete Project Role|
|[**rolesControllerGetAllProjectRoles**](#rolescontrollergetallprojectroles) | **GET** /projects/{projectId}/roles | Retrieve all roles|
|[**rolesControllerGetProjectRoleById**](#rolescontrollergetprojectrolebyid) | **GET** /projects/{projectId}/roles/{roleId} | Retrieve a role by ID|
|[**rolesControllerGetUserProjectRole**](#rolescontrollergetuserprojectrole) | **GET** /projects/{id}/members/role | Retrieve the role of a specific member|
|[**rolesControllerUpdateProjectRoleById**](#rolescontrollerupdateprojectrolebyid) | **PATCH** /projects/{projectId}/roles/{roleId} | Update a role|

# **rolesControllerCreateProjectRole**
> CreateProjectRoleResponseDto rolesControllerCreateProjectRole(createRoleDto)


### Example

```typescript
import {
    RolesApi,
    Configuration,
    CreateRoleDto
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new RolesApi(configuration);

let projectId: string; // (default to undefined)
let createRoleDto: CreateRoleDto; //

const { status, data } = await apiInstance.rolesControllerCreateProjectRole(
    projectId,
    createRoleDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createRoleDto** | **CreateRoleDto**|  | |
| **projectId** | [**string**] |  | defaults to undefined|


### Return type

**CreateProjectRoleResponseDto**

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

# **rolesControllerDeleteProjectRole**
> DeleteProjectRoleByIdResponseDto rolesControllerDeleteProjectRole()


### Example

```typescript
import {
    RolesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new RolesApi(configuration);

let projectId: string; // (default to undefined)
let roleId: number; // (default to undefined)

const { status, data } = await apiInstance.rolesControllerDeleteProjectRole(
    projectId,
    roleId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **roleId** | [**number**] |  | defaults to undefined|


### Return type

**DeleteProjectRoleByIdResponseDto**

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

# **rolesControllerGetAllProjectRoles**
> GetAllProjectRoleResponseDto rolesControllerGetAllProjectRoles()


### Example

```typescript
import {
    RolesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new RolesApi(configuration);

let projectId: string; // (default to undefined)
let page: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)
let column: string; // (optional) (default to undefined)
let direction: 'ASC' | 'DESC'; // (optional) (default to undefined)

const { status, data } = await apiInstance.rolesControllerGetAllProjectRoles(
    projectId,
    page,
    limit,
    column,
    direction
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


### Return type

**GetAllProjectRoleResponseDto**

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

# **rolesControllerGetProjectRoleById**
> GetProjectRoleByIdResponseDto rolesControllerGetProjectRoleById()


### Example

```typescript
import {
    RolesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new RolesApi(configuration);

let projectId: string; // (default to undefined)
let roleId: number; // (default to undefined)

const { status, data } = await apiInstance.rolesControllerGetProjectRoleById(
    projectId,
    roleId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **roleId** | [**number**] |  | defaults to undefined|


### Return type

**GetProjectRoleByIdResponseDto**

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

# **rolesControllerGetUserProjectRole**
> GetUserProjectRoleByRoleIdResponseDto rolesControllerGetUserProjectRole()


### Example

```typescript
import {
    RolesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new RolesApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.rolesControllerGetUserProjectRole(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**GetUserProjectRoleByRoleIdResponseDto**

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

# **rolesControllerUpdateProjectRoleById**
> UpdateProjectRoleResponseDto rolesControllerUpdateProjectRoleById(updateRoleByIdDto)


### Example

```typescript
import {
    RolesApi,
    Configuration,
    UpdateRoleByIdDto
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new RolesApi(configuration);

let projectId: string; // (default to undefined)
let roleId: number; // (default to undefined)
let updateRoleByIdDto: UpdateRoleByIdDto; //

const { status, data } = await apiInstance.rolesControllerUpdateProjectRoleById(
    projectId,
    roleId,
    updateRoleByIdDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateRoleByIdDto** | **UpdateRoleByIdDto**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **roleId** | [**number**] |  | defaults to undefined|


### Return type

**UpdateProjectRoleResponseDto**

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

