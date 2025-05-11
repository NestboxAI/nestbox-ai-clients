# AgentsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**agentManagementControllerCreateNewAgent**](#agentmanagementcontrollercreatenewagent) | **POST** /agents | |
|[**agentManagementControllerDeleteAgent**](#agentmanagementcontrollerdeleteagent) | **DELETE** /agents/{id} | |
|[**agentManagementControllerGetAllAgents**](#agentmanagementcontrollergetallagents) | **GET** /agents | |
|[**agentManagementControllerUpdateMachineAgent**](#agentmanagementcontrollerupdatemachineagent) | **PUT** /agents/{id} | |

# **agentManagementControllerCreateNewAgent**
> agentManagementControllerCreateNewAgent(createMachineAgentDto)


### Example

```typescript
import {
    AgentsApi,
    Configuration,
    CreateMachineAgentDto
} from '@nestbox-ai/instances';

const configuration = new Configuration();
const apiInstance = new AgentsApi(configuration);

let createMachineAgentDto: CreateMachineAgentDto; //

const { status, data } = await apiInstance.agentManagementControllerCreateNewAgent(
    createMachineAgentDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createMachineAgentDto** | **CreateMachineAgentDto**|  | |


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **agentManagementControllerDeleteAgent**
> agentManagementControllerDeleteAgent()


### Example

```typescript
import {
    AgentsApi,
    Configuration
} from '@nestbox-ai/instances';

const configuration = new Configuration();
const apiInstance = new AgentsApi(configuration);

let id: string; // (default to undefined)

const { status, data } = await apiInstance.agentManagementControllerDeleteAgent(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **agentManagementControllerGetAllAgents**
> agentManagementControllerGetAllAgents()


### Example

```typescript
import {
    AgentsApi,
    Configuration
} from '@nestbox-ai/instances';

const configuration = new Configuration();
const apiInstance = new AgentsApi(configuration);

let type: 'REGULAR' | 'CHAT'; //Type of agent. (optional) (default to undefined)

const { status, data } = await apiInstance.agentManagementControllerGetAllAgents(
    type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **type** | [**&#39;REGULAR&#39; | &#39;CHAT&#39;**]**Array<&#39;REGULAR&#39; &#124; &#39;CHAT&#39;>** | Type of agent. | (optional) defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **agentManagementControllerUpdateMachineAgent**
> agentManagementControllerUpdateMachineAgent(body)


### Example

```typescript
import {
    AgentsApi,
    Configuration
} from '@nestbox-ai/instances';

const configuration = new Configuration();
const apiInstance = new AgentsApi(configuration);

let id: string; // (default to undefined)
let body: object; //

const { status, data } = await apiInstance.agentManagementControllerUpdateMachineAgent(
    id,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **object**|  | |
| **id** | [**string**] |  | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

