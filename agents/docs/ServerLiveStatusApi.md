# ServerLiveStatusApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**appControllerGetStatus**](#appcontrollergetstatus) | **GET** / | |

# **appControllerGetStatus**
> appControllerGetStatus()


### Example

```typescript
import {
    ServerLiveStatusApi,
    Configuration
} from '@nestbox-ai/agents';

const configuration = new Configuration();
const apiInstance = new ServerLiveStatusApi(configuration);

const { status, data } = await apiInstance.appControllerGetStatus();
```

### Parameters
This endpoint does not have any parameters.


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

