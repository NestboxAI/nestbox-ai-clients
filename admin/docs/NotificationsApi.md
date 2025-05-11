# NotificationsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**notificationsControllerGetLastFiveNotifications**](#notificationscontrollergetlastfivenotifications) | **GET** /projects/{projectId}/notifications | Retrieve last notifications|
|[**notificationsControllerMarkNotificationsAsRead**](#notificationscontrollermarknotificationsasread) | **PUT** /projects/{projectId}/notifications/status | Mark notification as read|

# **notificationsControllerGetLastFiveNotifications**
> object notificationsControllerGetLastFiveNotifications()


### Example

```typescript
import {
    NotificationsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new NotificationsApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.notificationsControllerGetLastFiveNotifications(
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

# **notificationsControllerMarkNotificationsAsRead**
> object notificationsControllerMarkNotificationsAsRead(body)


### Example

```typescript
import {
    NotificationsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new NotificationsApi(configuration);

let projectId: string; // (default to undefined)
let body: object; //

const { status, data } = await apiInstance.notificationsControllerMarkNotificationsAsRead(
    projectId,
    body
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **body** | **object**|  | |
| **projectId** | [**string**] |  | defaults to undefined|


### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
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

