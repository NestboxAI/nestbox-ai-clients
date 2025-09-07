## @nestbox-ai/agents@1.0.50

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
npm install @nestbox-ai/agents@1.0.50 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ChatApi* | [**agentOperationsChatControllerCreateQuery**](docs/ChatApi.md#agentoperationschatcontrollercreatequery) | **POST** /agents/{id}/chat | 
*EventLogsApi* | [**agentOperationsEventLogsControllerGetEventLogs**](docs/EventLogsApi.md#agentoperationseventlogscontrollergeteventlogs) | **GET** /agents/{id}/events | 
*EventLogsApi* | [**agentOperationsEventLogsControllerGetEventLogsByQueryId**](docs/EventLogsApi.md#agentoperationseventlogscontrollergeteventlogsbyqueryid) | **GET** /agents/{id}/eventsByQueryId | 
*GuardrailsApi* | [**agentOperationsGuardrailsControllerCreateGuardrails**](docs/GuardrailsApi.md#agentoperationsguardrailscontrollercreateguardrails) | **POST** /agents/{id}/guardrails | 
*GuardrailsApi* | [**agentOperationsGuardrailsControllerDeleteGuardrails**](docs/GuardrailsApi.md#agentoperationsguardrailscontrollerdeleteguardrails) | **DELETE** /agents/{id}/guardrails/{guardrailsId} | 
*GuardrailsApi* | [**agentOperationsGuardrailsControllerGetAllGuardrails**](docs/GuardrailsApi.md#agentoperationsguardrailscontrollergetallguardrails) | **GET** /agents/{id}/guardrails | 
*GuardrailsApi* | [**agentOperationsGuardrailsControllerGetGuardrails**](docs/GuardrailsApi.md#agentoperationsguardrailscontrollergetguardrails) | **GET** /agents/{id}/guardrails/{guardrailsId} | 
*GuardrailsApi* | [**agentOperationsGuardrailsControllerUpdateGuardrails**](docs/GuardrailsApi.md#agentoperationsguardrailscontrollerupdateguardrails) | **PUT** /agents/{id}/guardrails/{guardrailsId} | 
*QueryApi* | [**agentOperationsQueryControllerCreateQuery**](docs/QueryApi.md#agentoperationsquerycontrollercreatequery) | **POST** /agents/{id}/query | 
*ServerLiveStatusApi* | [**appControllerGetStatus**](docs/ServerLiveStatusApi.md#appcontrollergetstatus) | **GET** / | 
*WebhooksApi* | [**agentOperationsWebhooksControllerCreateWebhook**](docs/WebhooksApi.md#agentoperationswebhookscontrollercreatewebhook) | **POST** /agents/{id}/webhooks | 
*WebhooksApi* | [**agentOperationsWebhooksControllerDeleteWebhook**](docs/WebhooksApi.md#agentoperationswebhookscontrollerdeletewebhook) | **DELETE** /agents/{id}/webhooks/{webhookId} | 
*WebhooksApi* | [**agentOperationsWebhooksControllerGetAllWebhooks**](docs/WebhooksApi.md#agentoperationswebhookscontrollergetallwebhooks) | **GET** /agents/{id}/webhooks | 
*WebhooksApi* | [**agentOperationsWebhooksControllerGetWebhook**](docs/WebhooksApi.md#agentoperationswebhookscontrollergetwebhook) | **GET** /agents/{id}/webhooks/{webhookId} | 
*WebhooksApi* | [**agentOperationsWebhooksControllerUpdateWebhook**](docs/WebhooksApi.md#agentoperationswebhookscontrollerupdatewebhook) | **PUT** /agents/{id}/webhooks/{webhookId} | 


### Documentation For Models

 - [AdHocCallbackDto](docs/AdHocCallbackDto.md)
 - [CreateGuardrailDto](docs/CreateGuardrailDto.md)
 - [CreateWebhookDto](docs/CreateWebhookDto.md)
 - [GuardrailUserDto](docs/GuardrailUserDto.md)
 - [MessageDto](docs/MessageDto.md)
 - [QueryHandlerDto](docs/QueryHandlerDto.md)
 - [UpdateWebhookDto](docs/UpdateWebhookDto.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.

