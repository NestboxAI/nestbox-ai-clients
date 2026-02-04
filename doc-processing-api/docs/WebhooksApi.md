# WebhooksApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**webhooksControllerCreateWebhook**](#webhookscontrollercreatewebhook) | **POST** /webhooks | Create webhook|
|[**webhooksControllerDeleteWebhook**](#webhookscontrollerdeletewebhook) | **DELETE** /webhooks/{webhookId} | Delete webhook|
|[**webhooksControllerGetWebhook**](#webhookscontrollergetwebhook) | **GET** /webhooks/{webhookId} | Read webhook|
|[**webhooksControllerListWebhooks**](#webhookscontrollerlistwebhooks) | **GET** /webhooks | List webhooks|
|[**webhooksControllerUpdateWebhook**](#webhookscontrollerupdatewebhook) | **PATCH** /webhooks/{webhookId} | Update webhook|

# **webhooksControllerCreateWebhook**
> WebhookDto webhooksControllerCreateWebhook(createWebhookInputDto)


### Example

```typescript
import {
    WebhooksApi,
    Configuration,
    CreateWebhookInputDto
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let createWebhookInputDto: CreateWebhookInputDto; //

const { status, data } = await apiInstance.webhooksControllerCreateWebhook(
    createWebhookInputDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createWebhookInputDto** | **CreateWebhookInputDto**|  | |


### Return type

**WebhookDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Webhook created |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhooksControllerDeleteWebhook**
> WebhookDto webhooksControllerDeleteWebhook()


### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let webhookId: string; //Webhook ID. (default to undefined)

const { status, data } = await apiInstance.webhooksControllerDeleteWebhook(
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] | Webhook ID. | defaults to undefined|


### Return type

**WebhookDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Webhook deleted |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhooksControllerGetWebhook**
> WebhookDto webhooksControllerGetWebhook()


### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let webhookId: string; //Webhook ID. (default to undefined)

const { status, data } = await apiInstance.webhooksControllerGetWebhook(
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **webhookId** | [**string**] | Webhook ID. | defaults to undefined|


### Return type

**WebhookDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Webhook details |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhooksControllerListWebhooks**
> PaginatedWebhooksDto webhooksControllerListWebhooks()


### Example

```typescript
import {
    WebhooksApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let page: number; //1-based page number. (optional) (default to 1)
let limit: number; //Page size. (optional) (default to 10)

const { status, data } = await apiInstance.webhooksControllerListWebhooks(
    page,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | 1-based page number. | (optional) defaults to 1|
| **limit** | [**number**] | Page size. | (optional) defaults to 10|


### Return type

**PaginatedWebhooksDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Paginated list of webhooks |  -  |
|**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhooksControllerUpdateWebhook**
> WebhookDto webhooksControllerUpdateWebhook(updateWebhookBodyInputDto)


### Example

```typescript
import {
    WebhooksApi,
    Configuration,
    UpdateWebhookBodyInputDto
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new WebhooksApi(configuration);

let webhookId: string; //Webhook ID. (default to undefined)
let updateWebhookBodyInputDto: UpdateWebhookBodyInputDto; //

const { status, data } = await apiInstance.webhooksControllerUpdateWebhook(
    webhookId,
    updateWebhookBodyInputDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateWebhookBodyInputDto** | **UpdateWebhookBodyInputDto**|  | |
| **webhookId** | [**string**] | Webhook ID. | defaults to undefined|


### Return type

**WebhookDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Webhook updated |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

