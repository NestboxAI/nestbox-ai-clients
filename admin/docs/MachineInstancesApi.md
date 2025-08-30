# MachineInstancesApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**machineInstancesControllerCreateMachineInstance**](#machineinstancescontrollercreatemachineinstance) | **POST** /projects/{projectId}/instances | Create Machine Instance|
|[**machineInstancesControllerDeleteMachineInstance**](#machineinstancescontrollerdeletemachineinstance) | **DELETE** /projects/{projectId}/instances | Delete machine instances by ids|
|[**machineInstancesControllerGetInstanceRunningStatus**](#machineinstancescontrollergetinstancerunningstatus) | **GET** /projects/{projectId}/instances/status | Retrieve running status of instances|
|[**machineInstancesControllerGetMachineBenchmarkingDatapoints**](#machineinstancescontrollergetmachinebenchmarkingdatapoints) | **GET** /projects/{projectId}/instances/machine/{machineId}/benchmarking-datapoints | Retrieve CSV benchmarking datapoints for a specific machine|
|[**machineInstancesControllerGetMachineBenchmarkingReports**](#machineinstancescontrollergetmachinebenchmarkingreports) | **GET** /projects/{projectId}/instances/machine/{machineId}/benchmarking-reports | Retrieve benchmarking reports for a specific machine|
|[**machineInstancesControllerGetMachineBootstrapStatus**](#machineinstancescontrollergetmachinebootstrapstatus) | **GET** /projects/{projectId}/instances/machine/{machineId}/status | Retrieve status of a specific machine instance|
|[**machineInstancesControllerGetMachineInstanceById**](#machineinstancescontrollergetmachineinstancebyid) | **GET** /projects/{projectId}/instances/machine/{machineId} | Retrieve running status of instances|
|[**machineInstancesControllerGetMachineInstanceByUserId**](#machineinstancescontrollergetmachineinstancebyuserid) | **GET** /projects/{projectId}/instances | Retrieve all machine instances with count|
|[**machineInstancesControllerUpdateRunningStatus**](#machineinstancescontrollerupdaterunningstatus) | **PUT** /projects/{projectId}/instances/status | Update Machine Instance Running Status|

# **machineInstancesControllerCreateMachineInstance**
> object machineInstancesControllerCreateMachineInstance()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerCreateMachineInstance(
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

# **machineInstancesControllerDeleteMachineInstance**
> object machineInstancesControllerDeleteMachineInstance()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerDeleteMachineInstance(
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

# **machineInstancesControllerGetInstanceRunningStatus**
> object machineInstancesControllerGetInstanceRunningStatus()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerGetInstanceRunningStatus(
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

# **machineInstancesControllerGetMachineBenchmarkingDatapoints**
> BenchmarkingDatapointDto machineInstancesControllerGetMachineBenchmarkingDatapoints()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)
let machineId: string; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerGetMachineBenchmarkingDatapoints(
    projectId,
    machineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **machineId** | [**string**] |  | defaults to undefined|


### Return type

**BenchmarkingDatapointDto**

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

# **machineInstancesControllerGetMachineBenchmarkingReports**
> BenchmarkingReportsDto machineInstancesControllerGetMachineBenchmarkingReports()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)
let machineId: string; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerGetMachineBenchmarkingReports(
    projectId,
    machineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **machineId** | [**string**] |  | defaults to undefined|


### Return type

**BenchmarkingReportsDto**

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

# **machineInstancesControllerGetMachineBootstrapStatus**
> MachineStatusDto machineInstancesControllerGetMachineBootstrapStatus()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)
let machineId: string; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerGetMachineBootstrapStatus(
    projectId,
    machineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **machineId** | [**string**] |  | defaults to undefined|


### Return type

**MachineStatusDto**

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

# **machineInstancesControllerGetMachineInstanceById**
> object machineInstancesControllerGetMachineInstanceById()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)
let machineId: string; // (default to undefined)
let page: number; // (default to undefined)
let limit: number; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerGetMachineInstanceById(
    projectId,
    machineId,
    page,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **machineId** | [**string**] |  | defaults to undefined|
| **page** | [**number**] |  | defaults to undefined|
| **limit** | [**number**] |  | defaults to undefined|


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

# **machineInstancesControllerGetMachineInstanceByUserId**
> object machineInstancesControllerGetMachineInstanceByUserId()


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)
let page: number; // (default to undefined)
let limit: number; // (default to undefined)

const { status, data } = await apiInstance.machineInstancesControllerGetMachineInstanceByUserId(
    projectId,
    page,
    limit
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **page** | [**number**] |  | defaults to undefined|
| **limit** | [**number**] |  | defaults to undefined|


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

# **machineInstancesControllerUpdateRunningStatus**
> object machineInstancesControllerUpdateRunningStatus(body)


### Example

```typescript
import {
    MachineInstancesApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new MachineInstancesApi(configuration);

let projectId: string; // (default to undefined)
let body: object; //

const { status, data } = await apiInstance.machineInstancesControllerUpdateRunningStatus(
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

