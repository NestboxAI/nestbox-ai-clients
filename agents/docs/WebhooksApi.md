# WebhooksApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**agentOperationsWebhooksControllerCreateWebhook**](#agentoperationswebhookscontrollercreatewebhook) | **POST** /agents/{id}/webhooks | |
|[**agentOperationsWebhooksControllerDeleteWebhook**](#agentoperationswebhookscontrollerdeletewebhook) | **DELETE** /agents/{id}/webhooks/{webhookId} | |
|[**agentOperationsWebhooksControllerGetAllWebhooks**](#agentoperationswebhookscontrollergetallwebhooks) | **GET** /agents/{id}/webhooks | |
|[**agentOperationsWebhooksControllerGetWebhook**](#agentoperationswebhookscontrollergetwebhook) | **GET** /agents/{id}/webhooks/{webhookId} | |
|[**agentOperationsWebhooksControllerUpdateWebhook**](#agentoperationswebhookscontrollerupdatewebhook) | **PUT** /agents/{id}/webhooks/{webhookId} | |

# **agentOperationsWebhooksControllerCreateWebhook**
> agentOperationsWebhooksControllerCreateWebhook(createWebhookDto)


### Example

```typescript
import {
    WebhooksApi,
    Configuration,
    CreateWebhookDto
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let createWebhookDto: CreateWebhookDto; //

const { status, data } = await apiInstance.agentOperationsWebhooksControllerCreateWebhook(
    id,
    createWebhookDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createWebhookDto** | **CreateWebhookDto**|  | |
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

# **agentOperationsWebhooksControllerDeleteWebhook**
> agentOperationsWebhooksControllerDeleteWebhook()


### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let webhookId: string; //ID of the webhook. (default to undefined)

const { status, data } = await apiInstance.agentOperationsWebhooksControllerDeleteWebhook(
    id,
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **webhookId** | [**string**] | ID of the webhook. | defaults to undefined|


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

# **agentOperationsWebhooksControllerGetAllWebhooks**
> agentOperationsWebhooksControllerGetAllWebhooks()


### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //ID of the agent. (default to undefined)

const { status, data } = await apiInstance.agentOperationsWebhooksControllerGetAllWebhooks(
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

# **agentOperationsWebhooksControllerGetWebhook**
> agentOperationsWebhooksControllerGetWebhook()


### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let webhookId: string; //ID of the webhook. (default to undefined)

const { status, data } = await apiInstance.agentOperationsWebhooksControllerGetWebhook(
    id,
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **webhookId** | [**string**] | ID of the webhook. | defaults to undefined|


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

# **agentOperationsWebhooksControllerUpdateWebhook**
> agentOperationsWebhooksControllerUpdateWebhook(updateWebhookDto)


### Example

```typescript
import {
    WebhooksApi,
    Configuration,
    UpdateWebhookDto
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let webhookId: string; //ID of the webhook. (default to undefined)
let updateWebhookDto: UpdateWebhookDto; //

const { status, data } = await apiInstance.agentOperationsWebhooksControllerUpdateWebhook(
    id,
    webhookId,
    updateWebhookDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateWebhookDto** | **UpdateWebhookDto**|  | |
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **webhookId** | [**string**] | ID of the webhook. | defaults to undefined|


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

