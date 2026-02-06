## @nestbox-ai/doc-processing-api@1.0.66

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
npm install @nestbox-ai/doc-processing-api@1.0.66 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ArtifactsApi* | [**artifactsControllerDownloadDocumentArtifacts**](docs/ArtifactsApi.md#artifactscontrollerdownloaddocumentartifacts) | **GET** /documents/{documentId}/artifacts | Download document artifacts
*DocumentsApi* | [**documentsControllerCreateDocument**](docs/DocumentsApi.md#documentscontrollercreatedocument) | **POST** /documents | Create document processing job
*DocumentsApi* | [**documentsControllerGetDocument**](docs/DocumentsApi.md#documentscontrollergetdocument) | **GET** /documents/{documentId} | Read document
*DocumentsApi* | [**documentsControllerListDocuments**](docs/DocumentsApi.md#documentscontrollerlistdocuments) | **GET** /documents | List documents
*EvalsApi* | [**evalsControllerCreateEval**](docs/EvalsApi.md#evalscontrollercreateeval) | **POST** /documents/{documentId}/evals | Create an eval from YAML
*EvalsApi* | [**evalsControllerGetEval**](docs/EvalsApi.md#evalscontrollergeteval) | **GET** /documents/{documentId}/evals/{evalId} | Read eval
*EvalsApi* | [**evalsControllerListEvals**](docs/EvalsApi.md#evalscontrollerlistevals) | **GET** /documents/{documentId}/evals | List evals for a document
*EvalsApi* | [**evalsControllerValidateEvalYaml**](docs/EvalsApi.md#evalscontrollervalidateevalyaml) | **POST** /documents/{documentId}/evals/validate | Validate eval YAML
*HealthApi* | [**healthControllerGetHealth**](docs/HealthApi.md#healthcontrollergethealth) | **GET** /health | Get system health
*JobsApi* | [**jobsControllerGetJob**](docs/JobsApi.md#jobscontrollergetjob) | **GET** /jobs/{jobId} | Read job
*JobsApi* | [**jobsControllerGetJobStatus**](docs/JobsApi.md#jobscontrollergetjobstatus) | **GET** /jobs/{jobId}/status | Get job status
*JobsApi* | [**jobsControllerListJobs**](docs/JobsApi.md#jobscontrollerlistjobs) | **GET** /jobs | List jobs
*ProfilesApi* | [**profilesControllerCreateProfile**](docs/ProfilesApi.md#profilescontrollercreateprofile) | **POST** /profiles | Create profile from YAML
*ProfilesApi* | [**profilesControllerGetProfile**](docs/ProfilesApi.md#profilescontrollergetprofile) | **GET** /profiles/{profileId} | Read profile
*ProfilesApi* | [**profilesControllerGetProfileSchema**](docs/ProfilesApi.md#profilescontrollergetprofileschema) | **GET** /profiles/schema | Get profile schema
*ProfilesApi* | [**profilesControllerListProfiles**](docs/ProfilesApi.md#profilescontrollerlistprofiles) | **GET** /profiles | List profiles
*QueriesApi* | [**queriesControllerCreateQuery**](docs/QueriesApi.md#queriescontrollercreatequery) | **POST** /query | Create batch query from YAML
*QueriesApi* | [**queriesControllerGetQuery**](docs/QueriesApi.md#queriescontrollergetquery) | **GET** /query/{queryId} | Read batch query
*QueriesApi* | [**queriesControllerListQueries**](docs/QueriesApi.md#queriescontrollerlistqueries) | **GET** /query | List batch queries
*QueriesApi* | [**queriesControllerValidateQueryYaml**](docs/QueriesApi.md#queriescontrollervalidatequeryyaml) | **POST** /query/validate | Validate batch query YAML
*SourcesApi* | [**sourcesControllerGetDocumentSources**](docs/SourcesApi.md#sourcescontrollergetdocumentsources) | **GET** /documents/{documentId}/sources | Read document sources
*WebhooksApi* | [**webhooksControllerCreateWebhook**](docs/WebhooksApi.md#webhookscontrollercreatewebhook) | **POST** /webhooks | Create webhook
*WebhooksApi* | [**webhooksControllerDeleteWebhook**](docs/WebhooksApi.md#webhookscontrollerdeletewebhook) | **DELETE** /webhooks/{webhookId} | Delete webhook
*WebhooksApi* | [**webhooksControllerGetWebhook**](docs/WebhooksApi.md#webhookscontrollergetwebhook) | **GET** /webhooks/{webhookId} | Read webhook
*WebhooksApi* | [**webhooksControllerListWebhooks**](docs/WebhooksApi.md#webhookscontrollerlistwebhooks) | **GET** /webhooks | List webhooks
*WebhooksApi* | [**webhooksControllerUpdateWebhook**](docs/WebhooksApi.md#webhookscontrollerupdatewebhook) | **PATCH** /webhooks/{webhookId} | Update webhook


### Documentation For Models

 - [BatchQueryDto](docs/BatchQueryDto.md)
 - [CreateWebhookInputDto](docs/CreateWebhookInputDto.md)
 - [DocumentCreateResponseDto](docs/DocumentCreateResponseDto.md)
 - [DocumentDto](docs/DocumentDto.md)
 - [DocumentSourcesResponseDto](docs/DocumentSourcesResponseDto.md)
 - [ErrorDto](docs/ErrorDto.md)
 - [EvalCreateResponseDto](docs/EvalCreateResponseDto.md)
 - [EvalDto](docs/EvalDto.md)
 - [GpuDeviceDto](docs/GpuDeviceDto.md)
 - [GpuHealthCheckDto](docs/GpuHealthCheckDto.md)
 - [HealthCheckItemDto](docs/HealthCheckItemDto.md)
 - [HealthChecksDto](docs/HealthChecksDto.md)
 - [HealthResponseDto](docs/HealthResponseDto.md)
 - [JobDto](docs/JobDto.md)
 - [JobLinksDto](docs/JobLinksDto.md)
 - [JobStatusDto](docs/JobStatusDto.md)
 - [PaginatedDocumentsDto](docs/PaginatedDocumentsDto.md)
 - [PaginatedEvalsDto](docs/PaginatedEvalsDto.md)
 - [PaginatedJobsDto](docs/PaginatedJobsDto.md)
 - [PaginatedProfilesDto](docs/PaginatedProfilesDto.md)
 - [PaginatedQueriesDto](docs/PaginatedQueriesDto.md)
 - [PaginatedWebhooksDto](docs/PaginatedWebhooksDto.md)
 - [PaginationDto](docs/PaginationDto.md)
 - [ProfileDto](docs/ProfileDto.md)
 - [QueryCreateResponseDto](docs/QueryCreateResponseDto.md)
 - [SourceItemDto](docs/SourceItemDto.md)
 - [UpdateWebhookBodyInputDto](docs/UpdateWebhookBodyInputDto.md)
 - [ValidationErrorDto](docs/ValidationErrorDto.md)
 - [ValidationIssueDto](docs/ValidationIssueDto.md)
 - [ValidationResultDto](docs/ValidationResultDto.md)
 - [WebhookDto](docs/WebhookDto.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.

