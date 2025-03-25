# **OpenAPI Clients Generator**

This repository automates the generation of OpenAPI JSON specification files and corresponding client SDKs for interacting with our API across four specific client contexts:

* **Admin Client**

* **Instances Client**

* **Documents Client**

* **Agents Client**

Each client has its own dedicated OpenAPI specification and automatically generated SDK, streamlining the process of maintaining accurate, up-to-date, and consistent API integrations.

---

## **📂 Repository Structure**

```
/
├── specs/
│   ├── admin-openapi.json
│   ├── instances-openapi.json
│   ├── documents-openapi.json
│   └── agents-openapi.json
├── clients/
│   ├── admin/
│   ├── instances/
│   ├── documents/
│   └── agents/
├── .github/workflow/
│   └── generate-clients.sh
└── README.md
```

---

## **🚀 Getting Started**

### **Prerequisites**

* [Node.js](https://nodejs.org/) (LTS version recommended)

* [OpenAPI Generator CLI](https://openapi-generator.tech/docs/installation)

### **Installation**

Clone this repository:

```
git clone https://github.com/your-username/openapi-clients-generator.git
cd openapi-clients-generator
```

Install dependencies:

```
npm install
```

---

## **⚙️ Generating Clients**

To generate the OpenAPI JSON files and all client SDKs, run:

```
npm run generate
```

This script will:

1. Generate/update the OpenAPI specification JSON files.

2. Generate SDK clients for each target (Admin, Instances, Documents, Agents).

Generated

