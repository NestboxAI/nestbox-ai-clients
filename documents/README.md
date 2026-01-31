## @nestbox-ai/documents@1.0.63

This generator creates TypeScript/JavaScript client that utilizes [axios](https://github.com/axios/axios). The generated Node module can be used in the following environments:

Environment
* Node.js
* Webpack
* Browserify

Language level
* ES5 - you must have a Promises/A+ library installed
* ES6

Module system
* CommonJS
* ES6 module system

It can be used in both TypeScript and JavaScript. In TypeScript, the definition will be automatically resolved via `package.json`. ([Reference](https://www.typescriptlang.org/docs/handbook/declaration-files/consumption.html))

### Building

To build and compile the typescript sources to javascript use:
```
npm install
npm run build
```

### Publishing

First build the package then run `npm publish`

### Consuming

navigate to the folder of your consuming project and run one of the following commands.

_published:_

```
npm install @nestbox-ai/documents@1.0.63 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AppApi* | [**appControllerGetHello**](docs/AppApi.md#appcontrollergethello) | **GET** / | 
*CollectionApi* | [**collectionControllerAddDocToCollection**](docs/CollectionApi.md#collectioncontrolleradddoctocollection) | **POST** /collections/{collection_id}/docs | Add a new doc
*CollectionApi* | [**collectionControllerChunkFileToCollection**](docs/CollectionApi.md#collectioncontrollerchunkfiletocollection) | **POST** /collections/{collection_id}/docs/file | Use a file to chunk and add to collection
*CollectionApi* | [**collectionControllerCreateCollection**](docs/CollectionApi.md#collectioncontrollercreatecollection) | **POST** /collections | Create a new collection
*CollectionApi* | [**collectionControllerDeleteCollection**](docs/CollectionApi.md#collectioncontrollerdeletecollection) | **DELETE** /collections/{collection_id} | Delete a collection
*CollectionApi* | [**collectionControllerDeleteDoc**](docs/CollectionApi.md#collectioncontrollerdeletedoc) | **DELETE** /collections/{collection_id}/docs/{doc_id} | Delete doc by ID
*CollectionApi* | [**collectionControllerDeleteDocsByMetadata**](docs/CollectionApi.md#collectioncontrollerdeletedocsbymetadata) | **DELETE** /collections/{collection_id}/docs | Delete docs based on metadata filter
*CollectionApi* | [**collectionControllerGetCollection**](docs/CollectionApi.md#collectioncontrollergetcollection) | **GET** /collections/{collection_id} | Get a collection info
*CollectionApi* | [**collectionControllerGetCollections**](docs/CollectionApi.md#collectioncontrollergetcollections) | **GET** /collections | List all collections
*CollectionApi* | [**collectionControllerGetDocById**](docs/CollectionApi.md#collectioncontrollergetdocbyid) | **GET** /collections/{collection_id}/docs/{doc_id} | Retrieve doc by ID
*CollectionApi* | [**collectionControllerSimilaritySearch**](docs/CollectionApi.md#collectioncontrollersimilaritysearch) | **POST** /collections/{collection_id}/query | Similarity search query
*CollectionApi* | [**collectionControllerUpdateCollection**](docs/CollectionApi.md#collectioncontrollerupdatecollection) | **PUT** /collections/{collection_id} | Updates a collection
*CollectionApi* | [**collectionControllerUpdateDoc**](docs/CollectionApi.md#collectioncontrollerupdatedoc) | **PUT** /collections/{collection_id}/docs/{doc_id} | Update or upsert doc


### Documentation For Models

 - [BadRequestExceptionResponse](docs/BadRequestExceptionResponse.md)
 - [ChunkFileRequestDTO](docs/ChunkFileRequestDTO.md)
 - [CreateCollectionRequestDTO](docs/CreateCollectionRequestDTO.md)
 - [CreateDocumentRequestDTO](docs/CreateDocumentRequestDTO.md)
 - [FatalErrorExceptionResponse](docs/FatalErrorExceptionResponse.md)
 - [ForbiddenExceptionResponse](docs/ForbiddenExceptionResponse.md)
 - [MessageResponseDTO](docs/MessageResponseDTO.md)
 - [NotFoundExceptionResponse](docs/NotFoundExceptionResponse.md)
 - [SimilaritySearchQueryDTO](docs/SimilaritySearchQueryDTO.md)
 - [UnauthorizedExceptionResponse](docs/UnauthorizedExceptionResponse.md)
 - [UpdateDocumentRequestDTO](docs/UpdateDocumentRequestDTO.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.

