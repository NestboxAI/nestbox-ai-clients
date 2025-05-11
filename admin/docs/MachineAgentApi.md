# MachineAgentApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**machineAgentControllerCreateMachineAgent**](#machineagentcontrollercreatemachineagent) | **POST** /projects/{projectId}/agents | Create New Machine Agent|
|[**machineAgentControllerDeleteMachineAgents**](#machineagentcontrollerdeletemachineagents) | **DELETE** /projects/{projectId}/agents/{agentId} | Delete machine agent|
|[**machineAgentControllerGetMachineAgentByProjectId**](#machineagentcontrollergetmachineagentbyprojectid) | **GET** /projects/{projectId}/agents | Get all machine agent with count|
|[**machineAgentControllerUpdateMachineAgent**](#machineagentcontrollerupdatemachineagent) | **PATCH** /projects/{projectId}/agents/{agentId} | Update machine agent by id|

# **machineAgentControllerCreateMachineAgent**
> CreateMachineAgentDto machineAgentControllerCreateMachineAgent(createMachineAgentDto)


### Example

```typescript
import {
    MachineAgentApi,
    Configuration,
    CreateMachineAgentDto
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineAgentApi(configuration);

let projectId: string; // (default to undefined)
let createMachineAgentDto: CreateMachineAgentDto; //

const { status, data } = await apiInstance.machineAgentControllerCreateMachineAgent(
    projectId,
    createMachineAgentDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createMachineAgentDto** | **CreateMachineAgentDto**|  | |
| **projectId** | [**string**] |  | defaults to undefined|


### Return type

**CreateMachineAgentDto**

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

# **machineAgentControllerDeleteMachineAgents**
> CreateMachineAgentDto machineAgentControllerDeleteMachineAgents(requestBody)


### Example

```typescript
import {
    MachineAgentApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineAgentApi(configuration);

let projectId: string; // (default to undefined)
let agentId: string; // (default to undefined)
let requestBody: Array<string>; //

const { status, data } = await apiInstance.machineAgentControllerDeleteMachineAgents(
    projectId,
    agentId,
    requestBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **requestBody** | **Array<string>**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **agentId** | [**string**] |  | defaults to undefined|


### Return type

**CreateMachineAgentDto**

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

# **machineAgentControllerGetMachineAgentByProjectId**
> CreateMachineAgentDto machineAgentControllerGetMachineAgentByProjectId()


### Example

```typescript
import {
    MachineAgentApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineAgentApi(configuration);

let projectId: string; // (default to undefined)
let page: number; // (default to undefined)
let limit: number; // (default to undefined)
let type: string; // (default to undefined)

const { status, data } = await apiInstance.machineAgentControllerGetMachineAgentByProjectId(
    projectId,
    page,
    limit,
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **page** | [**number**] |  | defaults to undefined|
| **limit** | [**number**] |  | defaults to undefined|
| **type** | [**string**] |  | defaults to undefined|


### Return type

**CreateMachineAgentDto**

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

# **machineAgentControllerUpdateMachineAgent**
> CreateMachineAgentDto machineAgentControllerUpdateMachineAgent()


### Example

```typescript
import {
    MachineAgentApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineAgentApi(configuration);

let projectId: string; // (default to undefined)
let agentId: string; // (default to undefined)

const { status, data } = await apiInstance.machineAgentControllerUpdateMachineAgent(
    projectId,
    agentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **agentId** | [**string**] |  | defaults to undefined|


### Return type

**CreateMachineAgentDto**

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

