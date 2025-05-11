# ChatApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**agentOperationsChatControllerCreateQuery**](#agentoperationschatcontrollercreatequery) | **POST** /agents/{id}/chat | |

# **agentOperationsChatControllerCreateQuery**
> agentOperationsChatControllerCreateQuery(queryHandlerDto)


### Example

```typescript
import {
    ChatApi,
    Configuration,
    QueryHandlerDto
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new ChatApi(configuration);

let id: string; //ID of the agent. (default to undefined)
let queryHandlerDto: QueryHandlerDto; //

const { status, data } = await apiInstance.agentOperationsChatControllerCreateQuery(
    id,
    queryHandlerDto
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **queryHandlerDto** | **QueryHandlerDto**|  | |
| **id** | [**string**] | ID of the agent. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

