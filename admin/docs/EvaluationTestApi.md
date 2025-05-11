# EvaluationTestApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**evaluationTestControllerAddEvaluationTest**](#evaluationtestcontrolleraddevaluationtest) | **POST** /projects/{projectId}/evaluation-tests | Add new evaluation test.|
|[**evaluationTestControllerDeleteEvaluation**](#evaluationtestcontrollerdeleteevaluation) | **DELETE** /projects/{projectId}/evaluation-tests/{testId} | Delete evaluation|
|[**evaluationTestControllerExecuteEvaluation**](#evaluationtestcontrollerexecuteevaluation) | **PUT** /projects/{projectId}/evaluation-tests/{testId}/execute | Execute evaluation test.|
|[**evaluationTestControllerGetEvaluationTest**](#evaluationtestcontrollergetevaluationtest) | **GET** /projects/{projectId}/evaluation-tests/{modelId} | Fetch evaluation test.|
|[**evaluationTestControllerUpdateEvaluation**](#evaluationtestcontrollerupdateevaluation) | **PUT** /projects/{projectId}/evaluation-tests/{testId} | Update evaluation test|

# **evaluationTestControllerAddEvaluationTest**
> object evaluationTestControllerAddEvaluationTest()


### Example

```typescript
import {
    EvaluationTestApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new EvaluationTestApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.evaluationTestControllerAddEvaluationTest(
    projectId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|


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

# **evaluationTestControllerDeleteEvaluation**
> object evaluationTestControllerDeleteEvaluation()


### Example

```typescript
import {
    EvaluationTestApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new EvaluationTestApi(configuration);

let projectId: string; // (default to undefined)
let testId: string; // (default to undefined)

const { status, data } = await apiInstance.evaluationTestControllerDeleteEvaluation(
    projectId,
    testId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **testId** | [**string**] |  | defaults to undefined|


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

# **evaluationTestControllerExecuteEvaluation**
> object evaluationTestControllerExecuteEvaluation()


### Example

```typescript
import {
    EvaluationTestApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new EvaluationTestApi(configuration);

let projectId: string; // (default to undefined)
let testId: string; // (default to undefined)

const { status, data } = await apiInstance.evaluationTestControllerExecuteEvaluation(
    projectId,
    testId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **testId** | [**string**] |  | defaults to undefined|


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

# **evaluationTestControllerGetEvaluationTest**
> object evaluationTestControllerGetEvaluationTest()


### Example

```typescript
import {
    EvaluationTestApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new EvaluationTestApi(configuration);

let projectId: string; // (default to undefined)
let modelId: string; // (default to undefined)

const { status, data } = await apiInstance.evaluationTestControllerGetEvaluationTest(
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

# **evaluationTestControllerUpdateEvaluation**
> object evaluationTestControllerUpdateEvaluation()


### Example

```typescript
import {
    EvaluationTestApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new EvaluationTestApi(configuration);

let projectId: string; // (default to undefined)
let testId: string; // (default to undefined)

const { status, data } = await apiInstance.evaluationTestControllerUpdateEvaluation(
    projectId,
    testId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **testId** | [**string**] |  | defaults to undefined|


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

