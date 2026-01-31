# ArtifactsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**artifactsControllerDownloadDocumentArtifacts**](#artifactscontrollerdownloaddocumentartifacts) | **GET** /documents/{documentId}/artifacts | Download document artifacts|

# **artifactsControllerDownloadDocumentArtifacts**
> artifactsControllerDownloadDocumentArtifacts()

Downloads artifacts produced by the pipeline (e.g., GraphRAG outputs, DB snapshots, visualizations) as a single archive.

### Example

```typescript
import {
    ArtifactsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new ArtifactsApi(configuration);

let documentId: string; //Document ID. (default to undefined)

const { status, data } = await apiInstance.artifactsControllerDownloadDocumentArtifacts(
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|


### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Artifacts archive (application/zip) |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

