# SourcesApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**sourcesControllerGetDocumentSources**](#sourcescontrollergetdocumentsources) | **GET** /documents/{documentId}/sources | Read document sources|

# **sourcesControllerGetDocumentSources**
> DocumentSourcesResponseDto sourcesControllerGetDocumentSources()

Returns source data used to produce answers/results. If sourceId is provided, returns the matching source. Otherwise returns a list.

### Example

```typescript
import {
    SourcesApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new SourcesApi(configuration);

let documentId: string; //Document ID. (default to undefined)
let jobId: any; //Optional job ID to scope sources to a specific query job. (optional) (default to undefined)
let sourceId: any; //Optional source ID (full or partial) to retrieve a specific source. (optional) (default to undefined)

const { status, data } = await apiInstance.sourcesControllerGetDocumentSources(
    documentId,
    jobId,
    sourceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|
| **jobId** | **any** | Optional job ID to scope sources to a specific query job. | (optional) defaults to undefined|
| **sourceId** | **any** | Optional source ID (full or partial) to retrieve a specific source. | (optional) defaults to undefined|


### Return type

**DocumentSourcesResponseDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Source data |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

