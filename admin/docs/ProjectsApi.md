# ProjectsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**projectControllerCreateProject**](#projectcontrollercreateproject) | **POST** /projects | Create Project|
|[**projectControllerDeleteProjectById**](#projectcontrollerdeleteprojectbyid) | **DELETE** /projects/{id} | Delete project by id|
|[**projectControllerGetAllProjects**](#projectcontrollergetallprojects) | **GET** /projects | Get all projects|
|[**projectControllerGetProjectById**](#projectcontrollergetprojectbyid) | **GET** /projects/{id} | Get project by id|
|[**projectControllerUpdateProjectById**](#projectcontrollerupdateprojectbyid) | **PATCH** /projects/{id} | Update project by id|

# **projectControllerCreateProject**
> CreateProjectResponseDTO projectControllerCreateProject(createProjectDTO)


### Example

```typescript
import {
    ProjectsApi,
    Configuration,
    CreateProjectDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let createProjectDTO: CreateProjectDTO; //

const { status, data } = await apiInstance.projectControllerCreateProject(
    createProjectDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createProjectDTO** | **CreateProjectDTO**|  | |


### Return type

**CreateProjectResponseDTO**

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

# **projectControllerDeleteProjectById**
> DeleteProjectResponseDTO projectControllerDeleteProjectById()


### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.projectControllerDeleteProjectById(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**DeleteProjectResponseDTO**

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

# **projectControllerGetAllProjects**
> GetAllProjectsResponseDTO projectControllerGetAllProjects()


### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let page: number; // (optional) (default to undefined)
let limit: number; // (optional) (default to undefined)
let column: string; // (optional) (default to undefined)
let direction: 'ASC' | 'DESC'; // (optional) (default to undefined)

const { status, data } = await apiInstance.projectControllerGetAllProjects(
    page,
    limit,
    column,
    direction
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] |  | (optional) defaults to undefined|
| **limit** | [**number**] |  | (optional) defaults to undefined|
| **column** | [**string**] |  | (optional) defaults to undefined|
| **direction** | [**&#39;ASC&#39; | &#39;DESC&#39;**]**Array<&#39;ASC&#39; &#124; &#39;DESC&#39;>** |  | (optional) defaults to undefined|


### Return type

**GetAllProjectsResponseDTO**

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

# **projectControllerGetProjectById**
> GetProjectByIDResponseDTO projectControllerGetProjectById()


### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.projectControllerGetProjectById(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

**GetProjectByIDResponseDTO**

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

# **projectControllerUpdateProjectById**
> UpdateProjectByIDResponseDTO projectControllerUpdateProjectById(updateProjectByIdRequest)


### Example

```typescript
import {
    ProjectsApi,
    Configuration,
    UpdateProjectByIdRequest
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let id: string; // (default to undefined)
let updateProjectByIdRequest: UpdateProjectByIdRequest; //

const { status, data } = await apiInstance.projectControllerUpdateProjectById(
    id,
    updateProjectByIdRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateProjectByIdRequest** | **UpdateProjectByIdRequest**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

**UpdateProjectByIDResponseDTO**

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

