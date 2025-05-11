# EventLogsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**agentOperationsEventLogsControllerGetEventLogs**](#agentoperationseventlogscontrollergeteventlogs) | **GET** /agents/{id}/events | |
|[**agentOperationsEventLogsControllerGetEventLogsByQueryId**](#agentoperationseventlogscontrollergeteventlogsbyqueryid) | **GET** /agents/{id}/eventsByQueryId | |

# **agentOperationsEventLogsControllerGetEventLogs**
> agentOperationsEventLogsControllerGetEventLogs()


### Example

```typescript
import {
    EventLogsApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new EventLogsApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let page: string; // (default to undefined)
let limit: string; // (default to undefined)

const { status, data } = await apiInstance.agentOperationsEventLogsControllerGetEventLogs(
    id,
    page,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **page** | [**string**] |  | defaults to undefined|
| **limit** | [**string**] |  | defaults to undefined|


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

# **agentOperationsEventLogsControllerGetEventLogsByQueryId**
> agentOperationsEventLogsControllerGetEventLogsByQueryId()


### Example

```typescript
import {
    EventLogsApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new EventLogsApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let queryId: string; // (default to undefined)

const { status, data } = await apiInstance.agentOperationsEventLogsControllerGetEventLogsByQueryId(
    id,
    queryId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **id** | [**string**] | ID of the agent. | defaults to undefined|
| **queryId** | [**string**] |  | defaults to undefined|


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

