# DocumentProcessingApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**documentProcessingControllerCreateBatchQuery**](#documentprocessingcontrollercreatebatchquery) | **POST** /projects/{projectId}/document-processing/{instanceId}/queries | Create batch query from YAML file (multipart)|
|[**documentProcessingControllerCreateDocumentProcessingJob**](#documentprocessingcontrollercreatedocumentprocessingjob) | **POST** /projects/{projectId}/document-processing/{instanceId}/documents | Create document processing job by uploading file (multipart)|
|[**documentProcessingControllerCreateEval**](#documentprocessingcontrollercreateeval) | **POST** /projects/{projectId}/document-processing/{instanceId}/evals | Create evaluation from YAML file (multipart)|
|[**documentProcessingControllerCreateProfile**](#documentprocessingcontrollercreateprofile) | **POST** /projects/{projectId}/document-processing/{instanceId}/profiles | Create processing profile from YAML file (multipart)|
|[**documentProcessingControllerCreateWebhook**](#documentprocessingcontrollercreatewebhook) | **POST** /projects/{projectId}/document-processing/{instanceId}/webhooks | Create webhook for receiving notifications|
|[**documentProcessingControllerDeleteWebhook**](#documentprocessingcontrollerdeletewebhook) | **DELETE** /projects/{projectId}/document-processing/{instanceId}/webhooks/{webhookId} | Delete webhook|
|[**documentProcessingControllerDownloadDocumentArtifacts**](#documentprocessingcontrollerdownloaddocumentartifacts) | **GET** /projects/{projectId}/document-processing/{instanceId}/documents/{documentId}/artifacts | Download document artifacts as archive|
|[**documentProcessingControllerGetDocument**](#documentprocessingcontrollergetdocument) | **GET** /projects/{projectId}/document-processing/{instanceId}/documents/{documentId} | Get processed document by ID|
|[**documentProcessingControllerGetEval**](#documentprocessingcontrollergeteval) | **GET** /projects/{projectId}/document-processing/{instanceId}/documents/{documentId}/evals/{evalId} | Get evaluation details by document ID and eval ID|
|[**documentProcessingControllerGetHealth**](#documentprocessingcontrollergethealth) | **GET** /projects/{projectId}/document-processing/{instanceId}/health | Get document processing API client health|
|[**documentProcessingControllerGetJob**](#documentprocessingcontrollergetjob) | **GET** /projects/{projectId}/document-processing/{instanceId}/jobs/{jobId} | Get processing job details by ID|
|[**documentProcessingControllerGetJobStatus**](#documentprocessingcontrollergetjobstatus) | **GET** /projects/{projectId}/document-processing/{instanceId}/jobs/{jobId}/status | Get processing job status (lightweight)|
|[**documentProcessingControllerGetProfile**](#documentprocessingcontrollergetprofile) | **GET** /projects/{projectId}/document-processing/{instanceId}/profiles/{profileId} | Get processing profile by ID|
|[**documentProcessingControllerGetProfileSchema**](#documentprocessingcontrollergetprofileschema) | **GET** /projects/{projectId}/document-processing/{instanceId}/profiles/schema | Get profile schema for YAML configuration|
|[**documentProcessingControllerGetQuery**](#documentprocessingcontrollergetquery) | **GET** /projects/{projectId}/document-processing/{instanceId}/queries/{queryId} | Get batch query details by ID|
|[**documentProcessingControllerGetWebhook**](#documentprocessingcontrollergetwebhook) | **GET** /projects/{projectId}/document-processing/{instanceId}/webhooks/{webhookId} | Get webhook details by ID|
|[**documentProcessingControllerListDocuments**](#documentprocessingcontrollerlistdocuments) | **GET** /projects/{projectId}/document-processing/{instanceId}/documents | List processed documents with pagination and filters|
|[**documentProcessingControllerListEvals**](#documentprocessingcontrollerlistevals) | **GET** /projects/{projectId}/document-processing/{instanceId}/documents/{documentId}/evals | List evaluations for a document with pagination|
|[**documentProcessingControllerListJobs**](#documentprocessingcontrollerlistjobs) | **GET** /projects/{projectId}/document-processing/{instanceId}/jobs | List processing jobs with pagination|
|[**documentProcessingControllerListProfiles**](#documentprocessingcontrollerlistprofiles) | **GET** /projects/{projectId}/document-processing/{instanceId}/profiles | List processing profiles with pagination|
|[**documentProcessingControllerListQueries**](#documentprocessingcontrollerlistqueries) | **GET** /projects/{projectId}/document-processing/{instanceId}/queries | List batch queries with pagination and filters|
|[**documentProcessingControllerListWebhooks**](#documentprocessingcontrollerlistwebhooks) | **GET** /projects/{projectId}/document-processing/{instanceId}/webhooks | List webhooks with pagination|
|[**documentProcessingControllerUpdateWebhook**](#documentprocessingcontrollerupdatewebhook) | **PUT** /projects/{projectId}/document-processing/{instanceId}/webhooks/{webhookId} | Update webhook configuration|
|[**documentProcessingControllerValidateEvalYaml**](#documentprocessingcontrollervalidateevalyaml) | **POST** /projects/{projectId}/document-processing/{instanceId}/documents/{documentId}/evals/validate | Validate eval YAML without creating evaluation (multipart)|
|[**documentProcessingControllerValidateQueryYaml**](#documentprocessingcontrollervalidatequeryyaml) | **POST** /projects/{projectId}/document-processing/{instanceId}/queries/validate | Validate batch query YAML without creating query (multipart)|

# **documentProcessingControllerCreateBatchQuery**
> object documentProcessingControllerCreateBatchQuery()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerCreateBatchQuery(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerCreateDocumentProcessingJob**
> object documentProcessingControllerCreateDocumentProcessingJob()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerCreateDocumentProcessingJob(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerCreateEval**
> object documentProcessingControllerCreateEval()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerCreateEval(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerCreateProfile**
> object documentProcessingControllerCreateProfile()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerCreateProfile(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerCreateWebhook**
> object documentProcessingControllerCreateWebhook()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerCreateWebhook(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerDeleteWebhook**
> object documentProcessingControllerDeleteWebhook()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let webhookId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerDeleteWebhook(
    projectId,
    instanceId,
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **webhookId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerDownloadDocumentArtifacts**
> object documentProcessingControllerDownloadDocumentArtifacts()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let documentId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerDownloadDocumentArtifacts(
    projectId,
    instanceId,
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **documentId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetDocument**
> object documentProcessingControllerGetDocument()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let documentId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetDocument(
    projectId,
    instanceId,
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **documentId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetEval**
> object documentProcessingControllerGetEval()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let documentId: string; // (default to undefined)
let evalId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetEval(
    projectId,
    instanceId,
    documentId,
    evalId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **documentId** | [**string**] |  | defaults to undefined|
| **evalId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetHealth**
> object documentProcessingControllerGetHealth()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetHealth(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetJob**
> object documentProcessingControllerGetJob()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let jobId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetJob(
    projectId,
    instanceId,
    jobId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **jobId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetJobStatus**
> object documentProcessingControllerGetJobStatus()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let jobId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetJobStatus(
    projectId,
    instanceId,
    jobId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **jobId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetProfile**
> object documentProcessingControllerGetProfile()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let profileId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetProfile(
    projectId,
    instanceId,
    profileId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **profileId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetProfileSchema**
> object documentProcessingControllerGetProfileSchema()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetProfileSchema(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetQuery**
> object documentProcessingControllerGetQuery()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let queryId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetQuery(
    projectId,
    instanceId,
    queryId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **queryId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerGetWebhook**
> object documentProcessingControllerGetWebhook()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let webhookId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerGetWebhook(
    projectId,
    instanceId,
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **webhookId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerListDocuments**
> object documentProcessingControllerListDocuments()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerListDocuments(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerListEvals**
> object documentProcessingControllerListEvals()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let documentId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerListEvals(
    projectId,
    instanceId,
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **documentId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerListJobs**
> object documentProcessingControllerListJobs()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerListJobs(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerListProfiles**
> object documentProcessingControllerListProfiles()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerListProfiles(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerListQueries**
> object documentProcessingControllerListQueries()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerListQueries(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerListWebhooks**
> object documentProcessingControllerListWebhooks()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerListWebhooks(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerUpdateWebhook**
> object documentProcessingControllerUpdateWebhook()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let webhookId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerUpdateWebhook(
    projectId,
    instanceId,
    webhookId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **webhookId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerValidateEvalYaml**
> object documentProcessingControllerValidateEvalYaml()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let documentId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerValidateEvalYaml(
    projectId,
    instanceId,
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **documentId** | [**string**] |  | defaults to undefined|


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

# **documentProcessingControllerValidateQueryYaml**
> object documentProcessingControllerValidateQueryYaml()


### Example

```typescript
import {
    DocumentProcessingApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentProcessingApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentProcessingControllerValidateQueryYaml(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


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

