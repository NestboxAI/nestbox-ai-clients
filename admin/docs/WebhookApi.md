# WebhookApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**webhookControllerCreateWebhook**](#webhookcontrollercreatewebhook) | **POST** /projects/{projectId}/webhooks | Create webhook|
|[**webhookControllerDeleteWebhook**](#webhookcontrollerdeletewebhook) | **DELETE** /projects/{projectId}/webhooks/{modelId} | Delete webhook|
|[**webhookControllerFetchWebhook**](#webhookcontrollerfetchwebhook) | **GET** /projects/{projectId}/webhooks/{modelId} | Fetch webhook|
|[**webhookControllerUpdateWebhook**](#webhookcontrollerupdatewebhook) | **PUT** /projects/{projectId}/webhooks/{webhookId} | Update webhook|

# **webhookControllerCreateWebhook**
> CreateWebhookDto webhookControllerCreateWebhook()


### Example

```typescript
import {
    WebhookApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new WebhookApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.webhookControllerCreateWebhook(
    projectId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|


### Return type

**CreateWebhookDto**

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

# **webhookControllerDeleteWebhook**
> CreateWebhookDto webhookControllerDeleteWebhook()


### Example

```typescript
import {
    WebhookApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new WebhookApi(configuration);

let projectId: string; // (default to undefined)
let modelId: string; // (default to undefined)

const { status, data } = await apiInstance.webhookControllerDeleteWebhook(
    projectId,
    modelId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **modelId** | [**string**] |  | defaults to undefined|


### Return type

**CreateWebhookDto**

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

# **webhookControllerFetchWebhook**
> CreateWebhookDto webhookControllerFetchWebhook()


### Example

```typescript
import {
    WebhookApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new WebhookApi(configuration);

let projectId: string; // (default to undefined)
let modelId: string; // (default to undefined)
let isAgentWebhook: boolean; // (default to undefined)

const { status, data } = await apiInstance.webhookControllerFetchWebhook(
    projectId,
    modelId,
    isAgentWebhook
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **modelId** | [**string**] |  | defaults to undefined|
| **isAgentWebhook** | [**boolean**] |  | defaults to undefined|


### Return type

**CreateWebhookDto**

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

# **webhookControllerUpdateWebhook**
> CreateWebhookDto webhookControllerUpdateWebhook()


### Example

```typescript
import {
    WebhookApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new WebhookApi(configuration);

let webhookId: string; // (default to undefined)
let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.webhookControllerUpdateWebhook(
    webhookId,
    projectId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] |  | defaults to undefined|
| **projectId** | [**string**] |  | defaults to undefined|


### Return type

**CreateWebhookDto**

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

