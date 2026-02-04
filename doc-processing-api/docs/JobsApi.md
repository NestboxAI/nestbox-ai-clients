# JobsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**jobsControllerGetJob**](#jobscontrollergetjob) | **GET** /jobs/{jobId} | Read job|
|[**jobsControllerGetJobStatus**](#jobscontrollergetjobstatus) | **GET** /jobs/{jobId}/status | Get job status|
|[**jobsControllerListJobs**](#jobscontrollerlistjobs) | **GET** /jobs | List jobs|

# **jobsControllerGetJob**
> JobDto jobsControllerGetJob()


### Example

```typescript
import {
    JobsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new JobsApi(configuration);

let jobId: string; //Job ID. (default to undefined)

const { status, data } = await apiInstance.jobsControllerGetJob(
    jobId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **jobId** | [**string**] | Job ID. | defaults to undefined|


### Return type

**JobDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Job details |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **jobsControllerGetJobStatus**
> JobStatusDto jobsControllerGetJobStatus()

Returns a lightweight status payload suitable for polling.

### Example

```typescript
import {
    JobsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new JobsApi(configuration);

let jobId: string; //Job ID. (default to undefined)

const { status, data } = await apiInstance.jobsControllerGetJobStatus(
    jobId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **jobId** | [**string**] | Job ID. | defaults to undefined|


### Return type

**JobStatusDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Job status |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **jobsControllerListJobs**
> PaginatedJobsDto jobsControllerListJobs()

Lists jobs for document processing, evaluations, and query jobs.

### Example

```typescript
import {
    JobsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new JobsApi(configuration);

let page: number; //1-based page number. (optional) (default to 1)
let limit: number; //Page size. (optional) (default to 10)

const { status, data } = await apiInstance.jobsControllerListJobs(
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

**PaginatedJobsDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Paginated list of jobs |  -  |
|**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

