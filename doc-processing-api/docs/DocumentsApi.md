# DocumentsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**documentsControllerCreateDocument**](#documentscontrollercreatedocument) | **POST** /documents | Create document processing job|
|[**documentsControllerGetDocument**](#documentscontrollergetdocument) | **GET** /documents/{documentId} | Read document|
|[**documentsControllerListDocuments**](#documentscontrollerlistdocuments) | **GET** /documents | List documents|

# **documentsControllerCreateDocument**
> DocumentCreateResponseDto documentsControllerCreateDocument()

Upload a document file (pdf/md/html/docx/etc) via multipart form to start processing.

### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let profileId: string; //Profile/config ID to use for processing (maps to CLI --config). (default to undefined)
let file: File; //Document file to process (pdf/md/html/docx/etc). (default to undefined)
let stages: string; //Comma-separated stages to run (e.g., docling,chunking,graphrag). If omitted, auto-detected by server. (optional) (default to undefined)
let priority: string; // (optional) (default to 'normal')
let visualize: boolean; //Whether to generate graph visualization artifacts. (optional) (default to false)
let tags: Array<string>; //Optional tags to associate with the document (e.g., [\\\"invoice\\\", \\\"2024\\\"]). (optional) (default to undefined)

const { status, data } = await apiInstance.documentsControllerCreateDocument(
    profileId,
    file,
    stages,
    priority,
    visualize,
    tags
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **profileId** | [**string**] | Profile/config ID to use for processing (maps to CLI --config). | defaults to undefined|
| **file** | [**File**] | Document file to process (pdf/md/html/docx/etc). | defaults to undefined|
| **stages** | [**string**] | Comma-separated stages to run (e.g., docling,chunking,graphrag). If omitted, auto-detected by server. | (optional) defaults to undefined|
| **priority** | [**string**]**Array<&#39;low&#39; &#124; &#39;normal&#39; &#124; &#39;high&#39;>** |  | (optional) defaults to 'normal'|
| **visualize** | [**boolean**] | Whether to generate graph visualization artifacts. | (optional) defaults to false|
| **tags** | **Array&lt;string&gt;** | Optional tags to associate with the document (e.g., [\\\&quot;invoice\\\&quot;, \\\&quot;2024\\\&quot;]). | (optional) defaults to undefined|


### Return type

**DocumentCreateResponseDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Document accepted/created. Processing typically runs as a background job. |  -  |
|**400** | Bad request |  -  |
|**401** | Unauthorized |  -  |
|**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **documentsControllerGetDocument**
> DocumentDto documentsControllerGetDocument()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let documentId: string; //Document ID. (default to undefined)

const { status, data } = await apiInstance.documentsControllerGetDocument(
    documentId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **documentId** | [**string**] | Document ID. | defaults to undefined|


### Return type

**DocumentDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Document details |  -  |
|**401** | Unauthorized |  -  |
|**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **documentsControllerListDocuments**
> PaginatedDocumentsDto documentsControllerListDocuments()

List processed documents. Supports filtering by profileId.

### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/doc-processing-api';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let page: number; //1-based page number. (optional) (default to 1)
let limit: number; //Page size. (optional) (default to 10)
let profileId: string; //Filter documents by profile/config ID. (optional) (default to undefined)
let tags: Array<string>; //Filter documents by tags (any match). Pass multiple times or comma-separated. (optional) (default to undefined)

const { status, data } = await apiInstance.documentsControllerListDocuments(
    page,
    limit,
    profileId,
    tags
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | [**number**] | 1-based page number. | (optional) defaults to 1|
| **limit** | [**number**] | Page size. | (optional) defaults to 10|
| **profileId** | [**string**] | Filter documents by profile/config ID. | (optional) defaults to undefined|
| **tags** | **Array&lt;string&gt;** | Filter documents by tags (any match). Pass multiple times or comma-separated. | (optional) defaults to undefined|


### Return type

**PaginatedDocumentsDto**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Paginated list of documents |  -  |
|**401** | Unauthorized |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

