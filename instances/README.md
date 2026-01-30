## @nestbox-ai/instances@1.0.58

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
npm install @nestbox-ai/instances@1.0.58 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AgentsApi* | [**agentManagementControllerCreateNewAgent**](docs/AgentsApi.md#agentmanagementcontrollercreatenewagent) | **POST** /agents | 
*AgentsApi* | [**agentManagementControllerDeleteAgent**](docs/AgentsApi.md#agentmanagementcontrollerdeleteagent) | **DELETE** /agents/{id} | 
*AgentsApi* | [**agentManagementControllerGetAllAgents**](docs/AgentsApi.md#agentmanagementcontrollergetallagents) | **GET** /agents | 
*AgentsApi* | [**agentManagementControllerUpdateMachineAgent**](docs/AgentsApi.md#agentmanagementcontrollerupdatemachineagent) | **PUT** /agents/{id} | 
*ManifestApi* | [**agentManagementManifestControllerGetManifest**](docs/ManifestApi.md#agentmanagementmanifestcontrollergetmanifest) | **GET** /manifest | 
*ServerLiveStatusApi* | [**appControllerGetStatus**](docs/ServerLiveStatusApi.md#appcontrollergetstatus) | **GET** / | 


### Documentation For Models

 - [CreateMachineAgentDto](docs/CreateMachineAgentDto.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.

