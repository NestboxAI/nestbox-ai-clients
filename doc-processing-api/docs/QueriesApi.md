# QueriesApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**queriesControllerCreateQuery**](#queriescontrollercreatequery) | **POST** /query | Create batch query from YAML|
|[**queriesControllerGetQuery**](#queriescontrollergetquery) | **GET** /query/{queryId} | Read batch query|
|[**queriesControllerListQueries**](#queriescontrollerlistqueries) | **GET** /query | List batch queries|
|[**queriesControllerValidateQueryYaml**](#queriescontrollervalidatequeryyaml) | **POST** /query/validate | Validate batch query YAML|

# **queriesControllerCreateQuery**
> QueryCreateResponseDto queriesControllerCreateQuery()

Uploads a batch queries YAML (multipart form). Typically schedules a job.

### Example

```typescript
import {
    QueriesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new QueriesApi(configuration);

let yaml: File; //Batch queries YAML file. (default to undefined)
let watch: boolean; // (optional) (default to false)

const { status, data } = await apiInstance.queriesControllerCreateQuery(
    yaml,
    watch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **yaml** | [**File**] | Batch queries YAML file. | defaults to undefined|
| **watch** | [**boolean**] |  | (optional) defaults to false|


### Return type

**QueryCreateResponseDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Batch query created |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |
|**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **queriesControllerGetQuery**
> BatchQueryDto queriesControllerGetQuery()


### Example

```typescript
import {
    QueriesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new QueriesApi(configuration);

let queryId: string; //Batch query ID. (default to undefined)

const { status, data } = await apiInstance.queriesControllerGetQuery(
    queryId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **queryId** | [**string**] | Batch query ID. | defaults to undefined|


### Return type

**BatchQueryDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Batch query details |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **queriesControllerListQueries**
> PaginatedQueriesDto queriesControllerListQueries()

Lists batch query runs (submitted via YAML).

### Example

```typescript
import {
    QueriesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new QueriesApi(configuration);

let page: number; //1-based page number. (optional) (default to 1)
let limit: number; //Page size. (optional) (default to 10)
let documentId: string; //Filter by document ID. (optional) (default to undefined)

const { status, data } = await apiInstance.queriesControllerListQueries(
    page,
    limit,
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | 1-based page number. | (optional) defaults to 1|
| **limit** | [**number**] | Page size. | (optional) defaults to 10|
| **documentId** | [**string**] | Filter by document ID. | (optional) defaults to undefined|


### Return type

**PaginatedQueriesDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Paginated list of batch queries |  -  |
|**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **queriesControllerValidateQueryYaml**
> ValidationResultDto queriesControllerValidateQueryYaml()

Validates an uploaded batch queries YAML without creating a query.

### Example

```typescript
import {
    QueriesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new QueriesApi(configuration);

let yaml: File; //YAML file to validate. (default to undefined)

const { status, data } = await apiInstance.queriesControllerValidateQueryYaml(
    yaml
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **yaml** | [**File**] | YAML file to validate. | defaults to undefined|


### Return type

**ValidationResultDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Validation result |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |
|**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

