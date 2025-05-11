# MachineAgentLogsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**logsControllerFetchEventLogs**](#logscontrollerfetcheventlogs) | **GET** /projects/{projectId}/fetchEventLogs/{agentId} | Fetch event logs.|

# **logsControllerFetchEventLogs**
> object logsControllerFetchEventLogs()


### Example

```typescript
import {
    MachineAgentLogsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineAgentLogsApi(configuration);

let projectId: string; // (default to undefined)
let agentId: string; // (default to undefined)

const { status, data } = await apiInstance.logsControllerFetchEventLogs(
    projectId,
    agentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **agentId** | [**string**] |  | defaults to undefined|


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

