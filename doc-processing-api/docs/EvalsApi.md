# EvalsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**evalsControllerCreateEval**](#evalscontrollercreateeval) | **POST** /documents/{documentId}/evals | Create an eval from YAML|
|[**evalsControllerGetEval**](#evalscontrollergeteval) | **GET** /documents/{documentId}/evals/{evalId} | Read eval|
|[**evalsControllerListEvals**](#evalscontrollerlistevals) | **GET** /documents/{documentId}/evals | List evals for a document|
|[**evalsControllerValidateEvalYaml**](#evalscontrollervalidateevalyaml) | **POST** /documents/{documentId}/evals/validate | Validate eval YAML|

# **evalsControllerCreateEval**
> EvalCreateResponseDto evalsControllerCreateEval()

Uploads an eval YAML (test cases) to run against a document.

### Example

```typescript
import {
    EvalsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new EvalsApi(configuration);

let documentId: string; //Document ID. (default to undefined)
let yaml: File; //Eval YAML file (test cases). (default to undefined)
let watch: boolean; //If true, server may keep the request open longer (optional); most clients should poll job status instead. (optional) (default to false)

const { status, data } = await apiInstance.evalsControllerCreateEval(
    documentId,
    yaml,
    watch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|
| **yaml** | [**File**] | Eval YAML file (test cases). | defaults to undefined|
| **watch** | [**boolean**] | If true, server may keep the request open longer (optional); most clients should poll job status instead. | (optional) defaults to false|


### Return type

**EvalCreateResponseDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Eval created (often schedules a job) |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |
|**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **evalsControllerGetEval**
> EvalDto evalsControllerGetEval()


### Example

```typescript
import {
    EvalsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new EvalsApi(configuration);

let documentId: string; //Document ID. (default to undefined)
let evalId: string; //Evaluation ID. (default to undefined)

const { status, data } = await apiInstance.evalsControllerGetEval(
    documentId,
    evalId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|
| **evalId** | [**string**] | Evaluation ID. | defaults to undefined|


### Return type

**EvalDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Eval details |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **evalsControllerListEvals**
> PaginatedEvalsDto evalsControllerListEvals()


### Example

```typescript
import {
    EvalsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new EvalsApi(configuration);

let documentId: string; //Document ID. (default to undefined)
let limit: any; //Page size. (optional) (default to undefined)
let page: any; //1-based page number. (optional) (default to undefined)

const { status, data } = await apiInstance.evalsControllerListEvals(
    documentId,
    limit,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|
| **limit** | **any** | Page size. | (optional) defaults to undefined|
| **page** | **any** | 1-based page number. | (optional) defaults to undefined|


### Return type

**PaginatedEvalsDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Paginated list of evaluations |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **evalsControllerValidateEvalYaml**
> ValidationResultDto evalsControllerValidateEvalYaml()

Validates an uploaded eval YAML without creating an eval.

### Example

```typescript
import {
    EvalsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new EvalsApi(configuration);

let documentId: string; //Document ID. (default to undefined)
let yaml: File; //YAML file to validate. (default to undefined)

const { status, data } = await apiInstance.evalsControllerValidateEvalYaml(
    documentId,
    yaml
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|
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
|**404** | Not found |  -  |
|**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

