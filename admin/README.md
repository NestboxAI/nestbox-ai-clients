## @nestbox-ai/admin@1.0.49

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
npm install @nestbox-ai/admin@1.0.49 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthApi* | [**authControllerExchangeToken**](docs/AuthApi.md#authcontrollerexchangetoken) | **POST** /auth/google/{token} | Exchange token
*AuthApi* | [**authControllerForgetPassword**](docs/AuthApi.md#authcontrollerforgetpassword) | **POST** /auth/forget-password | Forget password initiate
*AuthApi* | [**authControllerForgetPasswordVerification**](docs/AuthApi.md#authcontrollerforgetpasswordverification) | **POST** /auth/forget-password/verification | Forget password verification
*AuthApi* | [**authControllerLogin**](docs/AuthApi.md#authcontrollerlogin) | **POST** /auth/login | Login to the application
*AuthApi* | [**authControllerOAuthLogin**](docs/AuthApi.md#authcontrolleroauthlogin) | **POST** /auth/login/oauth | Login with OAuth apps
*AuthApi* | [**authControllerResetPassword**](docs/AuthApi.md#authcontrollerresetpassword) | **POST** /auth/reset-password | Forget password initiate
*AuthApi* | [**authControllerSignup**](docs/AuthApi.md#authcontrollersignup) | **POST** /auth/signup | Signup in the application
*DocumentsApi* | [**documentControllerAddDocToCollection**](docs/DocumentsApi.md#documentcontrolleradddoctocollection) | **POST** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs | Add a new doc
*DocumentsApi* | [**documentControllerAddDocToCollectionFromFile**](docs/DocumentsApi.md#documentcontrolleradddoctocollectionfromfile) | **POST** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/file | Use a file to chunk and add to collection
*DocumentsApi* | [**documentControllerCreateCollection**](docs/DocumentsApi.md#documentcontrollercreatecollection) | **POST** /projects/{projectId}/document/{instanceId}/collections | Create collection
*DocumentsApi* | [**documentControllerDeleteCollection**](docs/DocumentsApi.md#documentcontrollerdeletecollection) | **DELETE** /projects/{projectId}/document/{instanceId}/collections/{collectionId} | Delete collection
*DocumentsApi* | [**documentControllerDeleteDocById**](docs/DocumentsApi.md#documentcontrollerdeletedocbyid) | **DELETE** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/{docId} | Delete doc by ID
*DocumentsApi* | [**documentControllerDeleteDocsFromCollection**](docs/DocumentsApi.md#documentcontrollerdeletedocsfromcollection) | **DELETE** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs | Delete docs based on metadata filters
*DocumentsApi* | [**documentControllerGetAllCollections**](docs/DocumentsApi.md#documentcontrollergetallcollections) | **GET** /projects/{projectId}/document/{instanceId}/collections | Get all collections
*DocumentsApi* | [**documentControllerGetCollectionInfo**](docs/DocumentsApi.md#documentcontrollergetcollectioninfo) | **GET** /projects/{projectId}/document/{instanceId}/collections/{collectionId} | Get collection info
*DocumentsApi* | [**documentControllerGetDocById**](docs/DocumentsApi.md#documentcontrollergetdocbyid) | **GET** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/{docId} | Get doc by ID
*DocumentsApi* | [**documentControllerSimilaritySearch**](docs/DocumentsApi.md#documentcontrollersimilaritysearch) | **POST** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/query | Similarity search query
*DocumentsApi* | [**documentControllerUpdateCollection**](docs/DocumentsApi.md#documentcontrollerupdatecollection) | **PUT** /projects/{projectId}/document/{instanceId}/collections/{collectionId} | Update collection
*DocumentsApi* | [**documentControllerUpdateDoc**](docs/DocumentsApi.md#documentcontrollerupdatedoc) | **PUT** /projects/{projectId}/document/{instanceId}/collections/{collectionId}/docs/{docId} | Update or upsert doc
*EvaluationTestApi* | [**evaluationTestControllerAddEvaluationTest**](docs/EvaluationTestApi.md#evaluationtestcontrolleraddevaluationtest) | **POST** /projects/{projectId}/evaluation-tests | Add new evaluation test.
*EvaluationTestApi* | [**evaluationTestControllerDeleteEvaluation**](docs/EvaluationTestApi.md#evaluationtestcontrollerdeleteevaluation) | **DELETE** /projects/{projectId}/evaluation-tests/{testId} | Delete evaluation
*EvaluationTestApi* | [**evaluationTestControllerExecuteEvaluation**](docs/EvaluationTestApi.md#evaluationtestcontrollerexecuteevaluation) | **PUT** /projects/{projectId}/evaluation-tests/{testId}/execute | Execute evaluation test.
*EvaluationTestApi* | [**evaluationTestControllerGetEvaluationTest**](docs/EvaluationTestApi.md#evaluationtestcontrollergetevaluationtest) | **GET** /projects/{projectId}/evaluation-tests/{modelId} | Fetch evaluation test.
*EvaluationTestApi* | [**evaluationTestControllerUpdateEvaluation**](docs/EvaluationTestApi.md#evaluationtestcontrollerupdateevaluation) | **PUT** /projects/{projectId}/evaluation-tests/{testId} | Update evaluation test
*MachineAgentApi* | [**machineAgentControllerCreateMachineAgent**](docs/MachineAgentApi.md#machineagentcontrollercreatemachineagent) | **POST** /projects/{projectId}/agents | Create New Machine Agent
*MachineAgentApi* | [**machineAgentControllerDeleteMachineAgents**](docs/MachineAgentApi.md#machineagentcontrollerdeletemachineagents) | **DELETE** /projects/{projectId}/agents/{agentId} | Delete machine agent
*MachineAgentApi* | [**machineAgentControllerGetMachineAgentByProjectId**](docs/MachineAgentApi.md#machineagentcontrollergetmachineagentbyprojectid) | **GET** /projects/{projectId}/agents | Get all machine agent with count
*MachineAgentApi* | [**machineAgentControllerUpdateMachineAgent**](docs/MachineAgentApi.md#machineagentcontrollerupdatemachineagent) | **PATCH** /projects/{projectId}/agents/{agentId} | Update machine agent by id
*MachineAgentLogsApi* | [**logsControllerFetchAgentLogs**](docs/MachineAgentLogsApi.md#logscontrollerfetchagentlogs) | **GET** /projects/{projectId}/logs/{agentId} | Fetch agent logs.
*MachineAgentLogsApi* | [**logsControllerFetchEventLogs**](docs/MachineAgentLogsApi.md#logscontrollerfetcheventlogs) | **GET** /projects/{projectId}/fetchEventLogs/{agentId} | Fetch event logs.
*MachineInstancesApi* | [**machineInstancesControllerCreateMachineInstance**](docs/MachineInstancesApi.md#machineinstancescontrollercreatemachineinstance) | **POST** /projects/{projectId}/instances | Create Machine Instance
*MachineInstancesApi* | [**machineInstancesControllerDeleteMachineInstance**](docs/MachineInstancesApi.md#machineinstancescontrollerdeletemachineinstance) | **DELETE** /projects/{projectId}/instances | Delete machine instances by ids
*MachineInstancesApi* | [**machineInstancesControllerGetInstanceRunningStatus**](docs/MachineInstancesApi.md#machineinstancescontrollergetinstancerunningstatus) | **GET** /projects/{projectId}/instances/status | Retrieve running status of instances
*MachineInstancesApi* | [**machineInstancesControllerGetMachineBenchmarkingDatapoints**](docs/MachineInstancesApi.md#machineinstancescontrollergetmachinebenchmarkingdatapoints) | **GET** /projects/{projectId}/instances/machine/{machineId}/benchmarking-datapoints | Retrieve CSV benchmarking datapoints for a specific machine
*MachineInstancesApi* | [**machineInstancesControllerGetMachineBenchmarkingReports**](docs/MachineInstancesApi.md#machineinstancescontrollergetmachinebenchmarkingreports) | **GET** /projects/{projectId}/instances/machine/{machineId}/benchmarking-reports | Retrieve benchmarking reports for a specific machine
*MachineInstancesApi* | [**machineInstancesControllerGetMachineBootstrapStatus**](docs/MachineInstancesApi.md#machineinstancescontrollergetmachinebootstrapstatus) | **GET** /projects/{projectId}/instances/machine/{machineId}/status | Retrieve status of a specific machine instance
*MachineInstancesApi* | [**machineInstancesControllerGetMachineInstanceById**](docs/MachineInstancesApi.md#machineinstancescontrollergetmachineinstancebyid) | **GET** /projects/{projectId}/instances/machine/{machineId} | Retrieve running status of instances
*MachineInstancesApi* | [**machineInstancesControllerGetMachineInstanceByUserId**](docs/MachineInstancesApi.md#machineinstancescontrollergetmachineinstancebyuserid) | **GET** /projects/{projectId}/instances | Retrieve all machine instances with count
*MachineInstancesApi* | [**machineInstancesControllerUpdateRunningStatus**](docs/MachineInstancesApi.md#machineinstancescontrollerupdaterunningstatus) | **PUT** /projects/{projectId}/instances/status | Update Machine Instance Running Status
*MembersApi* | [**membersControllerAddTeamMemberToProject**](docs/MembersApi.md#memberscontrolleraddteammembertoproject) | **POST** /projects/{projectId}/members | Add a team member
*MembersApi* | [**membersControllerGetAllTeamMembersOfProject**](docs/MembersApi.md#memberscontrollergetallteammembersofproject) | **GET** /projects/{projectId}/members | Retrieve all team members
*MembersApi* | [**membersControllerUpdateTeamMemberRole**](docs/MembersApi.md#memberscontrollerupdateteammemberrole) | **PATCH** /projects/{projectId}/members/{memberId} | Update team member details
*MiscellaneousApi* | [**miscellaneousControllerGetData**](docs/MiscellaneousApi.md#miscellaneouscontrollergetdata) | **GET** /projects/machine/images | Get machine id matching instances.
*MiscellaneousApi* | [**miscellaneousControllerGetMachineInstanceByImageId**](docs/MiscellaneousApi.md#miscellaneouscontrollergetmachineinstancebyimageid) | **GET** /projects/{projectId}/allMachineInstance | Get machine id matching instances.
*MiscellaneousApi* | [**miscellaneousControllerUpdateTeamMemberStatus**](docs/MiscellaneousApi.md#miscellaneouscontrollerupdateteammemberstatus) | **PATCH** /projects/member/join | Join project
*NotificationsApi* | [**notificationsControllerGetLastFiveNotifications**](docs/NotificationsApi.md#notificationscontrollergetlastfivenotifications) | **GET** /projects/{projectId}/notifications | Retrieve last notifications
*NotificationsApi* | [**notificationsControllerMarkNotificationsAsRead**](docs/NotificationsApi.md#notificationscontrollermarknotificationsasread) | **PUT** /projects/{projectId}/notifications/status | Mark notification as read
*ProjectsApi* | [**projectControllerCreateProject**](docs/ProjectsApi.md#projectcontrollercreateproject) | **POST** /projects | Create Project
*ProjectsApi* | [**projectControllerDeleteProjectById**](docs/ProjectsApi.md#projectcontrollerdeleteprojectbyid) | **DELETE** /projects/{id} | Delete project by id
*ProjectsApi* | [**projectControllerGetAllProjects**](docs/ProjectsApi.md#projectcontrollergetallprojects) | **GET** /projects | Get all projects
*ProjectsApi* | [**projectControllerGetProjectById**](docs/ProjectsApi.md#projectcontrollergetprojectbyid) | **GET** /projects/{id} | Get project by id
*ProjectsApi* | [**projectControllerUpdateProjectById**](docs/ProjectsApi.md#projectcontrollerupdateprojectbyid) | **PATCH** /projects/{id} | Update project by id
*QueriesAndDocumentationsApi* | [**queriesAndDocControllerFetchSwaggerJSON**](docs/QueriesAndDocumentationsApi.md#queriesanddoccontrollerfetchswaggerjson) | **GET** /projects/{projectId}/{fieldName}/{modelId}/swagger | Fetch Swagger JSON
*QueriesAndDocumentationsApi* | [**queriesAndDocControllerRunQuery**](docs/QueriesAndDocumentationsApi.md#queriesanddoccontrollerrunquery) | **POST** /projects/{projectId}/queries | Run Query
*RolesApi* | [**rolesControllerCreateProjectRole**](docs/RolesApi.md#rolescontrollercreateprojectrole) | **POST** /projects/{projectId}/roles | Create a new role
*RolesApi* | [**rolesControllerDeleteProjectRole**](docs/RolesApi.md#rolescontrollerdeleteprojectrole) | **DELETE** /projects/{projectId}/roles/{roleId} | Delete Project Role
*RolesApi* | [**rolesControllerGetAllProjectRoles**](docs/RolesApi.md#rolescontrollergetallprojectroles) | **GET** /projects/{projectId}/roles | Retrieve all roles
*RolesApi* | [**rolesControllerGetProjectRoleById**](docs/RolesApi.md#rolescontrollergetprojectrolebyid) | **GET** /projects/{projectId}/roles/{roleId} | Retrieve a role by ID
*RolesApi* | [**rolesControllerGetUserProjectRole**](docs/RolesApi.md#rolescontrollergetuserprojectrole) | **GET** /projects/{id}/members/role | Retrieve the role of a specific member
*RolesApi* | [**rolesControllerUpdateProjectRoleById**](docs/RolesApi.md#rolescontrollerupdateprojectrolebyid) | **PATCH** /projects/{projectId}/roles/{roleId} | Update a role
*WebhookApi* | [**webhookControllerCreateWebhook**](docs/WebhookApi.md#webhookcontrollercreatewebhook) | **POST** /projects/{projectId}/webhooks | Create webhook
*WebhookApi* | [**webhookControllerDeleteWebhook**](docs/WebhookApi.md#webhookcontrollerdeletewebhook) | **DELETE** /projects/{projectId}/webhooks/{modelId} | Delete webhook
*WebhookApi* | [**webhookControllerFetchWebhook**](docs/WebhookApi.md#webhookcontrollerfetchwebhook) | **GET** /projects/{projectId}/webhooks/{modelId} | Fetch webhook
*WebhookApi* | [**webhookControllerUpdateWebhook**](docs/WebhookApi.md#webhookcontrollerupdatewebhook) | **PUT** /projects/{projectId}/webhooks/{webhookId} | Update webhook


### Documentation For Models

 - [AddProjectMemberData](docs/AddProjectMemberData.md)
 - [AddProjectMemberDto](docs/AddProjectMemberDto.md)
 - [AddProjectMemberResponseDTO](docs/AddProjectMemberResponseDTO.md)
 - [AllProjectResponse](docs/AllProjectResponse.md)
 - [AllProjectResponseModel](docs/AllProjectResponseModel.md)
 - [BadRequestExceptionResponse](docs/BadRequestExceptionResponse.md)
 - [BenchmarkingDatapointDto](docs/BenchmarkingDatapointDto.md)
 - [BenchmarkingReportsDto](docs/BenchmarkingReportsDto.md)
 - [BooleanResponseDTO](docs/BooleanResponseDTO.md)
 - [ChunkFileRequestDTO](docs/ChunkFileRequestDTO.md)
 - [CreateCollectionRequestDTO](docs/CreateCollectionRequestDTO.md)
 - [CreateDocumentRequestDTO](docs/CreateDocumentRequestDTO.md)
 - [CreateMachineAgentDto](docs/CreateMachineAgentDto.md)
 - [CreatePermissionDto](docs/CreatePermissionDto.md)
 - [CreateProjectDTO](docs/CreateProjectDTO.md)
 - [CreateProjectResponseDTO](docs/CreateProjectResponseDTO.md)
 - [CreateProjectRoleResponseDto](docs/CreateProjectRoleResponseDto.md)
 - [CreateResourceDto](docs/CreateResourceDto.md)
 - [CreateRoleDTO](docs/CreateRoleDTO.md)
 - [CreateRoleDto](docs/CreateRoleDto.md)
 - [CreateWebhookDto](docs/CreateWebhookDto.md)
 - [DeleteProjectDto](docs/DeleteProjectDto.md)
 - [DeleteProjectResponseDTO](docs/DeleteProjectResponseDTO.md)
 - [DeleteProjectRoleByIdResponseDto](docs/DeleteProjectRoleByIdResponseDto.md)
 - [FatalErrorExceptionResponse](docs/FatalErrorExceptionResponse.md)
 - [ForbiddenExceptionResponse](docs/ForbiddenExceptionResponse.md)
 - [ForgetPasswordRequestDTO](docs/ForgetPasswordRequestDTO.md)
 - [ForgetPasswordResponseDTO](docs/ForgetPasswordResponseDTO.md)
 - [ForgetPasswordVerificationRequestDTO](docs/ForgetPasswordVerificationRequestDTO.md)
 - [ForgetPasswordVerificationResponseDTO](docs/ForgetPasswordVerificationResponseDTO.md)
 - [GetAllProjectDto](docs/GetAllProjectDto.md)
 - [GetAllProjectMemberResponse](docs/GetAllProjectMemberResponse.md)
 - [GetAllProjectMemberResponseDto](docs/GetAllProjectMemberResponseDto.md)
 - [GetAllProjectRoleResponseDto](docs/GetAllProjectRoleResponseDto.md)
 - [GetAllProjectsResponseDTO](docs/GetAllProjectsResponseDTO.md)
 - [GetAllRoleDTO](docs/GetAllRoleDTO.md)
 - [GetProjectByIDResponseDTO](docs/GetProjectByIDResponseDTO.md)
 - [GetProjectRoleByIdResponseDto](docs/GetProjectRoleByIdResponseDto.md)
 - [GetRoleDTO](docs/GetRoleDTO.md)
 - [GetUserProjectRoleByRoleIdResponseDto](docs/GetUserProjectRoleByRoleIdResponseDto.md)
 - [LoginRequestDTO](docs/LoginRequestDTO.md)
 - [LoginResponseDTO](docs/LoginResponseDTO.md)
 - [MachineStatusDto](docs/MachineStatusDto.md)
 - [MessageResponseDTO](docs/MessageResponseDTO.md)
 - [NotFoundExceptionResponse](docs/NotFoundExceptionResponse.md)
 - [OAuthLoginRequestDTO](docs/OAuthLoginRequestDTO.md)
 - [PermissionsDTO](docs/PermissionsDTO.md)
 - [ProjectResponseModel](docs/ProjectResponseModel.md)
 - [ResetPasswordRequestDTO](docs/ResetPasswordRequestDTO.md)
 - [ResourceDTO](docs/ResourceDTO.md)
 - [RoleDto](docs/RoleDto.md)
 - [SignupRequestDTO](docs/SignupRequestDTO.md)
 - [SignupResponseDTO](docs/SignupResponseDTO.md)
 - [SimilaritySearchQueryDTO](docs/SimilaritySearchQueryDTO.md)
 - [TeamMemberDto](docs/TeamMemberDto.md)
 - [UnauthorizedExceptionResponse](docs/UnauthorizedExceptionResponse.md)
 - [UpdateDocumentRequestDTO](docs/UpdateDocumentRequestDTO.md)
 - [UpdatePermissionDto](docs/UpdatePermissionDto.md)
 - [UpdateProjectByIDResponseDTO](docs/UpdateProjectByIDResponseDTO.md)
 - [UpdateProjectByIdRequest](docs/UpdateProjectByIdRequest.md)
 - [UpdateProjectRoleResponseDto](docs/UpdateProjectRoleResponseDto.md)
 - [UpdateResourceDto](docs/UpdateResourceDto.md)
 - [UpdateRoleByIdDto](docs/UpdateRoleByIdDto.md)
 - [UpdateRoleDTO](docs/UpdateRoleDTO.md)
 - [UpdateTeamMemberRequestDTO](docs/UpdateTeamMemberRequestDTO.md)
 - [UpdateTeamMemberStatusRequestDTO](docs/UpdateTeamMemberStatusRequestDTO.md)
 - [UserDto](docs/UserDto.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization

Endpoints do not require authorization.

