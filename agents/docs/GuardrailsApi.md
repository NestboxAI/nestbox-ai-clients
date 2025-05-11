# GuardrailsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**agentOperationsGuardrailsControllerCreateGuardrails**](#agentoperationsguardrailscontrollercreateguardrails) | **POST** /agents/{id}/guardrails | |
|[**agentOperationsGuardrailsControllerDeleteGuardrails**](#agentoperationsguardrailscontrollerdeleteguardrails) | **DELETE** /agents/{id}/guardrails/{guardrailsId} | |
|[**agentOperationsGuardrailsControllerGetAllGuardrails**](#agentoperationsguardrailscontrollergetallguardrails) | **GET** /agents/{id}/guardrails | |
|[**agentOperationsGuardrailsControllerGetGuardrails**](#agentoperationsguardrailscontrollergetguardrails) | **GET** /agents/{id}/guardrails/{guardrailsId} | |
|[**agentOperationsGuardrailsControllerUpdateGuardrails**](#agentoperationsguardrailscontrollerupdateguardrails) | **PUT** /agents/{id}/guardrails/{guardrailsId} | |

# **agentOperationsGuardrailsControllerCreateGuardrails**
> agentOperationsGuardrailsControllerCreateGuardrails(createGuardrailDto)


### Example

```typescript
import {
    GuardrailsApi,
    Configuration,
    CreateGuardrailDto
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new GuardrailsApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let createGuardrailDto: CreateGuardrailDto; //

const { status, data } = await apiInstance.agentOperationsGuardrailsControllerCreateGuardrails(
    id,
    createGuardrailDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createGuardrailDto** | **CreateGuardrailDto**|  | |
| **id** | [**string**] | ID of the agent. | defaults to undefined|


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

# **agentOperationsGuardrailsControllerDeleteGuardrails**
> agentOperationsGuardrailsControllerDeleteGuardrails()


### Example

```typescript
import {
    GuardrailsApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new GuardrailsApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let guardrailsId: string; //ID of the guardrails. (default to undefined)

const { status, data } = await apiInstance.agentOperationsGuardrailsControllerDeleteGuardrails(
    id,
    guardrailsId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **guardrailsId** | [**string**] | ID of the guardrails. | defaults to undefined|


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

# **agentOperationsGuardrailsControllerGetAllGuardrails**
> agentOperationsGuardrailsControllerGetAllGuardrails()


### Example

```typescript
import {
    GuardrailsApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new GuardrailsApi(configuration);

let id: string; //ID of the agent. (default to undefined)

const { status, data } = await apiInstance.agentOperationsGuardrailsControllerGetAllGuardrails(
    id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|


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

# **agentOperationsGuardrailsControllerGetGuardrails**
> agentOperationsGuardrailsControllerGetGuardrails()


### Example

```typescript
import {
    GuardrailsApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new GuardrailsApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let guardrailsId: string; //ID of the guardrails. (default to undefined)

const { status, data } = await apiInstance.agentOperationsGuardrailsControllerGetGuardrails(
    id,
    guardrailsId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **guardrailsId** | [**string**] | ID of the guardrails. | defaults to undefined|


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

# **agentOperationsGuardrailsControllerUpdateGuardrails**
> agentOperationsGuardrailsControllerUpdateGuardrails(createGuardrailDto)


### Example

```typescript
import {
    GuardrailsApi,
    Configuration,
    CreateGuardrailDto
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new GuardrailsApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let guardrailsId: string; //ID of the guardrails. (default to undefined)
let createGuardrailDto: CreateGuardrailDto; //

const { status, data } = await apiInstance.agentOperationsGuardrailsControllerUpdateGuardrails(
    id,
    guardrailsId,
    createGuardrailDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createGuardrailDto** | **CreateGuardrailDto**|  | |
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **guardrailsId** | [**string**] | ID of the guardrails. | defaults to undefined|


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

