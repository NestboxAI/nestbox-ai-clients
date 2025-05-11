# QueriesAndDocumentationsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**queriesAndDocControllerFetchSwaggerJSON**](#queriesanddoccontrollerfetchswaggerjson) | **GET** /projects/{projectId}/{fieldName}/{modelId}/swagger | Fetch Swagger JSON|
|[**queriesAndDocControllerRunQuery**](#queriesanddoccontrollerrunquery) | **POST** /projects/{projectId}/queries | Run Query|

# **queriesAndDocControllerFetchSwaggerJSON**
> object queriesAndDocControllerFetchSwaggerJSON()


### Example

```typescript
import {
    QueriesAndDocumentationsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new QueriesAndDocumentationsApi(configuration);

let modelId: string; // (default to undefined)
let projectId: string; // (default to undefined)
let fieldName: string; // (default to undefined)

const { status, data } = await apiInstance.queriesAndDocControllerFetchSwaggerJSON(
    modelId,
    projectId,
    fieldName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **modelId** | [**string**] |  | defaults to undefined|
| **projectId** | [**string**] |  | defaults to undefined|
| **fieldName** | [**string**] |  | defaults to undefined|


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

# **queriesAndDocControllerRunQuery**
> CreateWebhookDto queriesAndDocControllerRunQuery()


### Example

```typescript
import {
    QueriesAndDocumentationsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new QueriesAndDocumentationsApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.queriesAndDocControllerRunQuery(
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

