# **Nestbox AI Clients**

This repository contains the official OpenAPI specifications and automatically generated TypeScript SDKs for the Nestbox AI Platform clients. The clients are designed to simplify integration, management, and scalability when building and deploying AI-driven agents and workflows.

## **Available Clients**

Each client provides distinct functionalities and maintains its own OpenAPI specification and SDK:

### **1\. Admin Client**

* Manage platform-wide configurations, projects, settings, and permissions.

* Monitor usage statistics and performance metrics.

* Oversee user and access management functionalities.

* Manage instances of documents and agents

### **2\. Instances Client**

* Create, configure, and manage individual instances of AI workflows.

* Monitor instance status and execution details.

* Scale and optimize instance resources and settings.

### **3\. Documents Client**

* Efficiently parse, catalog, tag, store, and manage documents.

* Query and retrieve documents through powerful search APIs.

* Integrate document handling seamlessly into your AI workflows.

### **4\. Agents Client**

* Deploy, configure, and manage intelligent AI agents.

* Integrate agents seamlessly with third-party services and APIs.

* Monitor agent performance, interactions, and outcomes.

## **OpenAPI Specifications**

Each client maintains a dedicated OpenAPI specification file in YAML format, located within the `specs/` directory:

```
specs/
├── admin-client.yaml
├── instances-client.yaml
├── documents-client.yaml
└── agents-client.yaml
```

## **TypeScript SDKs**

Automatically generated SDKs from OpenAPI specifications are available for easy integration into your TypeScript projects. SDKs reside in the `sdks/` directory:

```
sdks/
├── admin-client/
├── instances-client/
├── documents-client/
└── agents-client/
```

### **Installation**

Install the required SDK via npm or yarn. Example for the Documents Client:

```
npm install @nestbox/documents-client
# or
yarn add @nestbox/documents-client
```

### **Usage Example**

Basic usage example for Documents Client:

```
import { DocumentsClient } from '@nestbox/documents-client';

const documentsClient = new DocumentsClient({
  apiKey: 'YOUR_API_KEY',
  baseUrl: 'https://api.nestbox.ai/documents',
});

async function queryDocuments(query: string) {
  const results = await documentsClient.searchDocuments({ query });
  console.log(results);
}

queryDocuments('agent workflows');
```

## **Generating SDKs**

To regenerate SDKs from OpenAPI specifications, use the provided scripts:

```
npm run generate-sdks
```

Ensure your environment has [OpenAPI Generator CLI](https://github.com/OpenAPITools/openapi-generator-cli) installed.

## **Documentation**

Detailed API documentation is automatically generated from the OpenAPI specs and can be accessed online or locally by hosting the included YAML files in Swagger UI or similar tools.

## **Contributing**

Contributions, suggestions, and improvements are welcome\! Please create an issue or submit a pull request.

## **License**

This project is licensed under the MIT License. See [LICENSE](https://chatgpt.com/g/g-p-677d3b441f3c819188ef78cb69c1ffe1-nestbox/c/LICENSE) for details.
