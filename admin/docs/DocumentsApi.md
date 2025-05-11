# DocumentsApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**documentControllerAddDocToCollection**](#documentcontrolleradddoctocollection) | **POST** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs | Add a new doc|
|[**documentControllerAddDocToCollectionFromFile**](#documentcontrolleradddoctocollectionfromfile) | **POST** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/file | Use a file to chunk and add to collection|
|[**documentControllerCreateCollection**](#documentcontrollercreatecollection) | **POST** /projects/{projectId}/document/{instanceId}/collections | Create collection|
|[**documentControllerDeleteCollection**](#documentcontrollerdeletecollection) | **DELETE** /projects/{projectId}/document/{instanceId}/collections/{collectionId} | Delete collection|
|[**documentControllerDeleteDocById**](#documentcontrollerdeletedocbyid) | **DELETE** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/{docId} | Delete doc by ID|
|[**documentControllerDeleteDocsFromCollection**](#documentcontrollerdeletedocsfromcollection) | **DELETE** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs | Delete docs based on metadata filters|
|[**documentControllerGetAllCollections**](#documentcontrollergetallcollections) | **GET** /projects/{projectId}/document/{instanceId}/collections | Get all collections|
|[**documentControllerGetCollectionInfo**](#documentcontrollergetcollectioninfo) | **GET** /projects/{projectId}/document/{instanceId}/collections/{collectionId} | Get collection info|
|[**documentControllerGetDocById**](#documentcontrollergetdocbyid) | **GET** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/{docId} | Get doc by ID|
|[**documentControllerSimilaritySearch**](#documentcontrollersimilaritysearch) | **POST** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/query | Similarity search query|
|[**documentControllerUpdateCollection**](#documentcontrollerupdatecollection) | **PUT** /projects/{projectId}/document/{instanceId}/collections/{collectionId} | Update collection|
|[**documentControllerUpdateDoc**](#documentcontrollerupdatedoc) | **PUT** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/{docId} | Update or upsert doc|

# **documentControllerAddDocToCollection**
> MessageResponseDTO documentControllerAddDocToCollection(createDocumentRequestDTO)


### Example

```typescript
import {
    DocumentsApi,
    Configuration,
    CreateDocumentRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let createDocumentRequestDTO: CreateDocumentRequestDTO; //

const { status, data } = await apiInstance.documentControllerAddDocToCollection(
    projectId,
    instanceId,
    collectionId,
    createDocumentRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createDocumentRequestDTO** | **CreateDocumentRequestDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerAddDocToCollectionFromFile**
> MessageResponseDTO documentControllerAddDocToCollectionFromFile(chunkFileRequestDTO)


### Example

```typescript
import {
    DocumentsApi,
    Configuration,
    ChunkFileRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let chunkFileRequestDTO: ChunkFileRequestDTO; //

const { status, data } = await apiInstance.documentControllerAddDocToCollectionFromFile(
    projectId,
    instanceId,
    collectionId,
    chunkFileRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **chunkFileRequestDTO** | **ChunkFileRequestDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerCreateCollection**
> MessageResponseDTO documentControllerCreateCollection(createCollectionRequestDTO)


### Example

```typescript
import {
    DocumentsApi,
    Configuration,
    CreateCollectionRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let createCollectionRequestDTO: CreateCollectionRequestDTO; //

const { status, data } = await apiInstance.documentControllerCreateCollection(
    projectId,
    instanceId,
    createCollectionRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createCollectionRequestDTO** | **CreateCollectionRequestDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerDeleteCollection**
> MessageResponseDTO documentControllerDeleteCollection()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)

const { status, data } = await apiInstance.documentControllerDeleteCollection(
    projectId,
    instanceId,
    collectionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerDeleteDocById**
> MessageResponseDTO documentControllerDeleteDocById()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let docId: string; // (default to undefined)

const { status, data } = await apiInstance.documentControllerDeleteDocById(
    projectId,
    instanceId,
    collectionId,
    docId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|
| **docId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerDeleteDocsFromCollection**
> MessageResponseDTO documentControllerDeleteDocsFromCollection()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let filter: string; // (default to undefined)

const { status, data } = await apiInstance.documentControllerDeleteDocsFromCollection(
    projectId,
    instanceId,
    collectionId,
    filter
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|
| **filter** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerGetAllCollections**
> MessageResponseDTO documentControllerGetAllCollections()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)

const { status, data } = await apiInstance.documentControllerGetAllCollections(
    projectId,
    instanceId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerGetCollectionInfo**
> MessageResponseDTO documentControllerGetCollectionInfo()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)

const { status, data } = await apiInstance.documentControllerGetCollectionInfo(
    projectId,
    instanceId,
    collectionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerGetDocById**
> MessageResponseDTO documentControllerGetDocById()


### Example

```typescript
import {
    DocumentsApi,
    Configuration
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let docId: string; // (default to undefined)

const { status, data } = await apiInstance.documentControllerGetDocById(
    projectId,
    instanceId,
    collectionId,
    docId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|
| **docId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerSimilaritySearch**
> MessageResponseDTO documentControllerSimilaritySearch(similaritySearchQueryDTO)


### Example

```typescript
import {
    DocumentsApi,
    Configuration,
    SimilaritySearchQueryDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let similaritySearchQueryDTO: SimilaritySearchQueryDTO; //

const { status, data } = await apiInstance.documentControllerSimilaritySearch(
    projectId,
    instanceId,
    collectionId,
    similaritySearchQueryDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **similaritySearchQueryDTO** | **SimilaritySearchQueryDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerUpdateCollection**
> MessageResponseDTO documentControllerUpdateCollection(createCollectionRequestDTO)


### Example

```typescript
import {
    DocumentsApi,
    Configuration,
    CreateCollectionRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let createCollectionRequestDTO: CreateCollectionRequestDTO; //

const { status, data } = await apiInstance.documentControllerUpdateCollection(
    projectId,
    instanceId,
    collectionId,
    createCollectionRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createCollectionRequestDTO** | **CreateCollectionRequestDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

# **documentControllerUpdateDoc**
> MessageResponseDTO documentControllerUpdateDoc(updateDocumentRequestDTO)


### Example

```typescript
import {
    DocumentsApi,
    Configuration,
    UpdateDocumentRequestDTO
} from '@nestbox-ai/admin';

const configuration = new Configuration();
const apiInstance = new DocumentsApi(configuration);

let projectId: string; // (default to undefined)
let instanceId: string; // (default to undefined)
let collectionId: string; // (default to undefined)
let docId: string; // (default to undefined)
let updateDocumentRequestDTO: UpdateDocumentRequestDTO; //

const { status, data } = await apiInstance.documentControllerUpdateDoc(
    projectId,
    instanceId,
    collectionId,
    docId,
    updateDocumentRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateDocumentRequestDTO** | **UpdateDocumentRequestDTO**|  | |
| **projectId** | [**string**] |  | defaults to undefined|
| **instanceId** | [**string**] |  | defaults to undefined|
| **collectionId** | [**string**] |  | defaults to undefined|
| **docId** | [**string**] |  | defaults to undefined|


### Return type

**MessageResponseDTO**

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

