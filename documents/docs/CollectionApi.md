# CollectionApi

All URIs are relative to *http://localhost*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**collectionControllerAddDocToCollection**](#collectioncontrolleradddoctocollection) | **POST** /collections/{collection_id}/docs | Add a new doc|
|[**collectionControllerChunkFileToCollection**](#collectioncontrollerchunkfiletocollection) | **POST** /collections/{collection_id}/docs/file | Use a file to chunk and add to collection|
|[**collectionControllerCreateCollection**](#collectioncontrollercreatecollection) | **POST** /collections | Create a new collection|
|[**collectionControllerDeleteCollection**](#collectioncontrollerdeletecollection) | **DELETE** /collections/{collection_id} | Delete a collection|
|[**collectionControllerDeleteDoc**](#collectioncontrollerdeletedoc) | **DELETE** /collections/{collection_id}/docs/{doc_id} | Delete doc by ID|
|[**collectionControllerDeleteDocsByMetadata**](#collectioncontrollerdeletedocsbymetadata) | **DELETE** /collections/{collection_id}/docs | Delete docs based on metadata filter|
|[**collectionControllerGetCollection**](#collectioncontrollergetcollection) | **GET** /collections/{collection_id} | Get a collection info|
|[**collectionControllerGetCollections**](#collectioncontrollergetcollections) | **GET** /collections | List all collections|
|[**collectionControllerGetDocById**](#collectioncontrollergetdocbyid) | **GET** /collections/{collection_id}/docs/{doc_id} | Retrieve doc by ID|
|[**collectionControllerSimilaritySearch**](#collectioncontrollersimilaritysearch) | **POST** /collections/{collection_id}/query | Similarity search query|
|[**collectionControllerUpdateCollection**](#collectioncontrollerupdatecollection) | **PUT** /collections/{collection_id} | Updates a collection|
|[**collectionControllerUpdateDoc**](#collectioncontrollerupdatedoc) | **PUT** /collections/{collection_id}/docs/{doc_id} | Update or upsert doc|

# **collectionControllerAddDocToCollection**
> MessageResponseDTO collectionControllerAddDocToCollection(createDocumentRequestDTO)


### Example

```typescript
import {
    CollectionApi,
    Configuration,
    CreateDocumentRequestDTO
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let createDocumentRequestDTO: CreateDocumentRequestDTO; //

const { status, data } = await apiInstance.collectionControllerAddDocToCollection(
    collectionId,
    createDocumentRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createDocumentRequestDTO** | **CreateDocumentRequestDTO**|  | |
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

# **collectionControllerChunkFileToCollection**
> MessageResponseDTO collectionControllerChunkFileToCollection(chunkFileRequestDTO)


### Example

```typescript
import {
    CollectionApi,
    Configuration,
    ChunkFileRequestDTO
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let chunkFileRequestDTO: ChunkFileRequestDTO; //

const { status, data } = await apiInstance.collectionControllerChunkFileToCollection(
    collectionId,
    chunkFileRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **chunkFileRequestDTO** | **ChunkFileRequestDTO**|  | |
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

# **collectionControllerCreateCollection**
> MessageResponseDTO collectionControllerCreateCollection(createCollectionRequestDTO)


### Example

```typescript
import {
    CollectionApi,
    Configuration,
    CreateCollectionRequestDTO
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let createCollectionRequestDTO: CreateCollectionRequestDTO; //

const { status, data } = await apiInstance.collectionControllerCreateCollection(
    createCollectionRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createCollectionRequestDTO** | **CreateCollectionRequestDTO**|  | |


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

# **collectionControllerDeleteCollection**
> MessageResponseDTO collectionControllerDeleteCollection()


### Example

```typescript
import {
    CollectionApi,
    Configuration
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)

const { status, data } = await apiInstance.collectionControllerDeleteCollection(
    collectionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **collectionControllerDeleteDoc**
> MessageResponseDTO collectionControllerDeleteDoc()


### Example

```typescript
import {
    CollectionApi,
    Configuration
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let docId: string; // (default to undefined)

const { status, data } = await apiInstance.collectionControllerDeleteDoc(
    collectionId,
    docId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **collectionControllerDeleteDocsByMetadata**
> MessageResponseDTO collectionControllerDeleteDocsByMetadata()


### Example

```typescript
import {
    CollectionApi,
    Configuration
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let filter: string; // (default to undefined)

const { status, data } = await apiInstance.collectionControllerDeleteDocsByMetadata(
    collectionId,
    filter
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **collectionControllerGetCollection**
> MessageResponseDTO collectionControllerGetCollection()


### Example

```typescript
import {
    CollectionApi,
    Configuration
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)

const { status, data } = await apiInstance.collectionControllerGetCollection(
    collectionId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **collectionControllerGetCollections**
> MessageResponseDTO collectionControllerGetCollections()


### Example

```typescript
import {
    CollectionApi,
    Configuration
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

const { status, data } = await apiInstance.collectionControllerGetCollections();
```

### Parameters
This endpoint does not have any parameters.


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

# **collectionControllerGetDocById**
> MessageResponseDTO collectionControllerGetDocById()


### Example

```typescript
import {
    CollectionApi,
    Configuration
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let docId: string; // (default to undefined)

const { status, data } = await apiInstance.collectionControllerGetDocById(
    collectionId,
    docId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
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

# **collectionControllerSimilaritySearch**
> MessageResponseDTO collectionControllerSimilaritySearch(similaritySearchQueryDTO)


### Example

```typescript
import {
    CollectionApi,
    Configuration,
    SimilaritySearchQueryDTO
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let similaritySearchQueryDTO: SimilaritySearchQueryDTO; //

const { status, data } = await apiInstance.collectionControllerSimilaritySearch(
    collectionId,
    similaritySearchQueryDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **similaritySearchQueryDTO** | **SimilaritySearchQueryDTO**|  | |
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

# **collectionControllerUpdateCollection**
> MessageResponseDTO collectionControllerUpdateCollection(createCollectionRequestDTO)


### Example

```typescript
import {
    CollectionApi,
    Configuration,
    CreateCollectionRequestDTO
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let createCollectionRequestDTO: CreateCollectionRequestDTO; //

const { status, data } = await apiInstance.collectionControllerUpdateCollection(
    collectionId,
    createCollectionRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **createCollectionRequestDTO** | **CreateCollectionRequestDTO**|  | |
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

# **collectionControllerUpdateDoc**
> MessageResponseDTO collectionControllerUpdateDoc(updateDocumentRequestDTO)


### Example

```typescript
import {
    CollectionApi,
    Configuration,
    UpdateDocumentRequestDTO
} from '@nestbox-ai/documents';

const configuration = new Configuration();
const apiInstance = new CollectionApi(configuration);

let collectionId: string; // (default to undefined)
let docId: string; // (default to undefined)
let updateDocumentRequestDTO: UpdateDocumentRequestDTO; //

const { status, data } = await apiInstance.collectionControllerUpdateDoc(
    collectionId,
    docId,
    updateDocumentRequestDTO
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **updateDocumentRequestDTO** | **UpdateDocumentRequestDTO**|  | |
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

