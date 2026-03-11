# Nestbox AI Document Processing API — Usage Guide

This guide walks you through using the `@nestbox-ai/doc-processing-api` TypeScript client to interact with the Nestbox Documents Processing API. The library is auto-generated from OpenAPI and uses [axios](https://github.com/axios/axios) under the hood.

---

## Table of Contents

- [Installation](#installation)
- [Configuration](#configuration)
- [Quick Start — End-to-End Workflow](#quick-start--end-to-end-workflow)
- [API Reference by Domain](#api-reference-by-domain)
  - [Profiles](#profiles)
  - [Documents](#documents)
  - [Jobs](#jobs)
  - [Evals](#evals)
  - [Queries](#queries)
  - [Sources](#sources)
  - [Artifacts](#artifacts)
  - [Webhooks](#webhooks)
  - [Health](#health)
- [Pagination](#pagination)
- [Error Handling](#error-handling)
- [Models Reference](#models-reference)

---

## Installation

```bash
npm install @nestbox-ai/doc-processing-api
```

The only runtime dependency is `axios ^1.13.5`.

---

## Configuration

Every API class accepts an optional `Configuration` object that lets you set the base URL, authentication headers, and other request defaults.

```typescript
import { Configuration } from '@nestbox-ai/doc-processing-api';

const config = new Configuration({
  basePath: 'https://doc-processing.example.com', // your server URL
  baseOptions: {
    headers: {
      'Authorization': 'Bearer <YOUR_TOKEN>',
    },
  },
});
```

### Configuration Options

| Option | Type | Description |
|--------|------|-------------|
| `basePath` | `string` | Override the default base URL (`http://localhost`). |
| `apiKey` | `string \| (name: string) => string` | API key for key-based auth. |
| `accessToken` | `string \| (name?: string, scopes?: string[]) => string` | OAuth2 / Bearer token. |
| `username` / `password` | `string` | Basic auth credentials. |
| `baseOptions` | `object` | Default axios request options (headers, timeout, etc.). |
| `formDataCtor` | `new () => FormData` | Custom `FormData` constructor for environments that don't have a built-in one. |

---

## Quick Start — End-to-End Workflow

The typical workflow is: **create a profile → upload a document → poll the job → retrieve results**.

```typescript
import {
  Configuration,
  ProfilesApi,
  DocumentsApi,
  JobsApi,
  SourcesApi,
  ArtifactsApi,
} from '@nestbox-ai/doc-processing-api';
import * as fs from 'fs';

const config = new Configuration({
  basePath: 'https://doc-processing.example.com',
});

const profiles  = new ProfilesApi(config);
const documents = new DocumentsApi(config);
const jobs      = new JobsApi(config);
const sources   = new SourcesApi(config);
const artifacts = new ArtifactsApi(config);

async function processDocument() {
  // 1. Create a profile from a YAML config file
  const profileYaml = fs.createReadStream('./my-profile.yaml') as any;
  const { data: profile } = await profiles.profilesControllerCreateProfile(
    profileYaml,
    'my-extraction-profile',  // optional name override
    ['production', 'finance'] // optional tags
  );
  console.log('Profile created:', profile.id);

  // 2. Upload a document for processing
  const file = fs.createReadStream('./report.pdf') as any;
  const { data: createResponse } = await documents.documentsControllerCreateDocument(
    profile.id,   // profileId
    file,          // the document file
    undefined,     // stages (auto-detected)
    'normal',      // priority: 'low' | 'normal' | 'high'
    false,         // visualize
    ['invoice', '2024'] // tags
  );
  const documentId = createResponse.document.id;
  const jobId = createResponse.job.id;
  console.log('Document created:', documentId, '| Job:', jobId);

  // 3. Poll job status until completed
  let jobStatus;
  do {
    const { data } = await jobs.jobsControllerGetJobStatus(jobId);
    jobStatus = data;
    console.log(`Job ${jobId}: ${jobStatus.state} (${(jobStatus.progress ?? 0) * 100}%)`);
    if (jobStatus.state === 'completed' || jobStatus.state === 'failed') break;
    await new Promise((r) => setTimeout(r, 3000)); // wait 3s
  } while (true);

  if (jobStatus.state === 'failed') {
    console.error('Job failed:', jobStatus.error);
    return;
  }

  // 4. Read back the document (now with metrics)
  const { data: doc } = await documents.documentsControllerGetDocument(documentId);
  console.log('Document status:', doc.status, '| Metrics:', doc.metrics);

  // 5. Retrieve source chunks
  const { data: sourcesResponse } = await sources.sourcesControllerGetDocumentSources(documentId);
  console.log('Sources:', sourcesResponse.data.length, 'items');

  // 6. Download pipeline artifacts (zip)
  const { data: archive } = await artifacts.artifactsControllerDownloadDocumentArtifacts(documentId);
  console.log('Artifacts downloaded');
}

processDocument().catch(console.error);
```

---

## API Reference by Domain

### Profiles

Profiles are YAML configuration files that define how documents are processed (extraction rules, pipeline stages, etc.).

```typescript
import { ProfilesApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new ProfilesApi(new Configuration({ basePath: '...' }));
```

#### Create a Profile

Upload a YAML config file via multipart form:

```typescript
const yamlFile = fs.createReadStream('./config.yaml') as any;

const { data: profile } = await api.profilesControllerCreateProfile(
  yamlFile,          // yaml: File — the YAML config
  'my-profile-name', // name (optional) — overrides name from YAML
  ['tag1', 'tag2']   // tags (optional)
);
// profile: ProfileDto { id, name, description, createdAt, yamlFileName, ... }
```

#### Get a Profile

```typescript
const { data: profile } = await api.profilesControllerGetProfile('profile-id-here');
```

#### List Profiles

```typescript
const { data: paginated } = await api.profilesControllerListProfiles(
  1,  // page (1-based)
  20  // limit
);
// paginated: PaginatedProfilesDto { data: ProfileDto[], pagination: PaginationDto }
```

#### Get Profile Schema

Returns the JSON schema that YAML profiles must conform to:

```typescript
const { data: schema } = await api.profilesControllerGetProfileSchema();
```

---

### Documents

Documents represent files uploaded for processing (PDF, DOCX, HTML, Markdown, etc.).

```typescript
import { DocumentsApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new DocumentsApi(new Configuration({ basePath: '...' }));
```

#### Create a Document (Upload & Process)

Uploads a file and starts a background processing job:

```typescript
const file = fs.createReadStream('./document.pdf') as any;

const { data } = await api.documentsControllerCreateDocument(
  'profile-id',             // profileId — which profile/config to use
  file,                     // file — the document file
  'docling,chunking',       // stages (optional) — pipeline stages to run
  'high',                   // priority (optional) — 'low' | 'normal' | 'high'
  true,                     // visualize (optional) — generate graph artifacts
  ['invoice', 'quarterly']  // tags (optional)
);

// data: DocumentCreateResponseDto
// data.document — the created DocumentDto
// data.job      — the processing JobDto (use job.id to track progress)
```

#### Get a Document

```typescript
const { data: doc } = await api.documentsControllerGetDocument('document-id');
// doc: DocumentDto { id, profileId, status, fileName, contentType, sizeBytes, metrics, tags, ... }
```

**Document statuses:** `queued` → `processing` → `ready` | `failed` | `deleted`

#### List Documents

```typescript
const { data: paginated } = await api.documentsControllerListDocuments(
  1,              // page
  25,             // limit
  'profile-id',   // profileId filter (optional)
  ['finance']     // tags filter (optional)
);
```

---

### Jobs

Jobs track asynchronous processing operations (document processing, evaluations, batch queries).

```typescript
import { JobsApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new JobsApi(new Configuration({ basePath: '...' }));
```

#### Get Full Job Details

```typescript
const { data: job } = await api.jobsControllerGetJob('job-id');
// job: JobDto { id, type, state, progress, stage, message, error, links, metadata, ... }
```

**Job types:** `document_processing`, `evaluation`, `batch_query`, `other`
**Job states:** `pending` → `processing` → `completed` | `failed` | `canceled`

#### Poll Job Status (Lightweight)

Returns only essential status fields — ideal for polling loops:

```typescript
const { data: status } = await api.jobsControllerGetJobStatus('job-id');
// status: JobStatusDto { id, state, progress, stage, message, error, updatedAt }
```

#### List Jobs

```typescript
const { data: paginated } = await api.jobsControllerListJobs(
  1,  // page
  50  // limit
);
```

#### Polling Pattern

```typescript
async function waitForJob(api: JobsApi, jobId: string, intervalMs = 3000): Promise<JobStatusDto> {
  while (true) {
    const { data: status } = await api.jobsControllerGetJobStatus(jobId);
    if (status.state === 'completed' || status.state === 'failed' || status.state === 'canceled') {
      return status;
    }
    console.log(`[${jobId}] ${status.state} — ${status.stage ?? ''} (${((status.progress ?? 0) * 100).toFixed(0)}%)`);
    await new Promise((r) => setTimeout(r, intervalMs));
  }
}
```

---

### Evals

Evaluations let you run test cases (defined in YAML) against a processed document to measure accuracy and quality.

```typescript
import { EvalsApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new EvalsApi(new Configuration({ basePath: '...' }));
```

#### Create an Eval

```typescript
const yamlFile = fs.createReadStream('./test-cases.yaml') as any;

const { data } = await api.evalsControllerCreateEval(
  'document-id',  // documentId
  yamlFile,        // yaml — eval YAML file (test cases)
  false            // watch (optional) — if true, server may keep request open longer
);
// data: EvalCreateResponseDto { eval: EvalDto, job: JobDto }
```

#### Validate Eval YAML Before Submitting

Check your YAML for errors before creating an eval:

```typescript
const yamlFile = fs.createReadStream('./test-cases.yaml') as any;

const { data: validation } = await api.evalsControllerValidateEvalYaml(
  'document-id',
  yamlFile
);
// validation: ValidationResultDto { valid: boolean, warnings?: ValidationIssueDto[], normalized?: object }

if (!validation.valid) {
  console.error('YAML validation failed');
}
```

#### Get an Eval

```typescript
const { data: evalResult } = await api.evalsControllerGetEval('document-id', 'eval-id');
// evalResult: EvalDto { id, documentId, status, summary, report, ... }
```

**Eval statuses:** `queued` → `running` → `completed` | `failed`

#### List Evals for a Document

```typescript
const { data: paginated } = await api.evalsControllerListEvals(
  'document-id',
  1,   // page
  20   // limit
);
```

---

### Queries

Batch queries let you submit a set of questions (defined in YAML) to run against processed documents.

```typescript
import { QueriesApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new QueriesApi(new Configuration({ basePath: '...' }));
```

#### Create a Batch Query

```typescript
const yamlFile = fs.createReadStream('./queries.yaml') as any;

const { data } = await api.queriesControllerCreateQuery(
  yamlFile,  // yaml — batch queries YAML file
  false      // watch (optional)
);
// data: QueryCreateResponseDto { query: BatchQueryDto, job: JobDto }
```

#### Validate Query YAML Before Submitting

```typescript
const yamlFile = fs.createReadStream('./queries.yaml') as any;

const { data: validation } = await api.queriesControllerValidateQueryYaml(yamlFile);
// validation: ValidationResultDto { valid, warnings?, normalized? }
```

#### Get a Batch Query

```typescript
const { data: query } = await api.queriesControllerGetQuery('query-id');
// query: BatchQueryDto { id, documentId, status, results, ... }
```

**Query statuses:** `queued` → `running` → `completed` | `failed`

#### List Batch Queries

```typescript
const { data: paginated } = await api.queriesControllerListQueries(
  1,   // page
  20   // limit
);
```

---

### Sources

Sources represent the text chunks and data used to produce answers during queries.

```typescript
import { SourcesApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new SourcesApi(new Configuration({ basePath: '...' }));
```

#### Get Document Sources

```typescript
const { data: sourcesResponse } = await api.sourcesControllerGetDocumentSources(
  'document-id',
  'job-id',     // jobId (optional) — scope to a specific query job
  'source-id'   // sourceId (optional) — retrieve a specific source by ID
);
// sourcesResponse: DocumentSourcesResponseDto { data: SourceItemDto[] }

for (const source of sourcesResponse.data) {
  console.log(`[${source.id}] page=${source.page}, chunk=${source.chunkId}`);
  console.log(source.text);
}
```

Each `SourceItemDto` contains:
- `id` — unique source identifier
- `documentId` — parent document
- `jobId` — associated job
- `chunkId` — the chunk within the document
- `page` — page number
- `text` — the source text content
- `metadata` — additional key-value metadata

---

### Artifacts

Download pipeline artifacts (GraphRAG outputs, DB snapshots, visualizations) as a zip archive.

```typescript
import { ArtifactsApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new ArtifactsApi(new Configuration({ basePath: '...' }));
```

#### Download Document Artifacts

```typescript
const response = await api.artifactsControllerDownloadDocumentArtifacts('document-id');
// Response body is a zip archive (application/zip)
```

To save the archive to disk, configure axios to handle binary responses:

```typescript
const config = new Configuration({
  basePath: '...',
  baseOptions: { responseType: 'arraybuffer' },
});
const api = new ArtifactsApi(config);

const { data } = await api.artifactsControllerDownloadDocumentArtifacts('document-id');
fs.writeFileSync('./artifacts.zip', Buffer.from(data));
```

---

### Webhooks

Register webhook URLs to receive notifications when processing jobs complete or fail.

```typescript
import { WebhooksApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new WebhooksApi(new Configuration({ basePath: '...' }));
```

#### Create a Webhook

```typescript
const { data: webhook } = await api.webhooksControllerCreateWebhook({
  url: 'https://your-server.com/webhooks/doc-processing',
});
// webhook: WebhookDto { id, url, createdAt, updatedAt }
```

#### Get a Webhook

```typescript
const { data: webhook } = await api.webhooksControllerGetWebhook('webhook-id');
```

#### List Webhooks

```typescript
const { data: paginated } = await api.webhooksControllerListWebhooks(
  1,   // page
  20   // limit
);
```

#### Update a Webhook

```typescript
const { data: updated } = await api.webhooksControllerUpdateWebhook('webhook-id', {
  url: 'https://your-server.com/webhooks/new-endpoint',
});
```

#### Delete a Webhook

```typescript
await api.webhooksControllerDeleteWebhook('webhook-id');
```

---

### Health

Check the system health, including Redis, database, and GPU status.

```typescript
import { HealthApi, Configuration } from '@nestbox-ai/doc-processing-api';

const api = new HealthApi(new Configuration({ basePath: '...' }));

const { data: health } = await api.healthControllerGetHealth();
// health: HealthResponseDto { status, timestamp, checks }

console.log('Overall:', health.status);           // 'ok' | 'degraded' | 'down'
console.log('Redis:', health.checks.redis.status);
console.log('DB:', health.checks.db.status);
console.log('GPU:', health.checks.gpu.status, '— devices:', health.checks.gpu.deviceCount);
```

---

## Pagination

All list endpoints return a paginated response with the shape:

```typescript
interface PaginatedResponse<T> {
  data: T[];
  pagination: {
    page: number;   // current page (1-based)
    limit: number;  // page size
    total: number;  // total items across all pages
  };
}
```

Example — iterate through all documents:

```typescript
let page = 1;
const limit = 50;
let allDocuments: DocumentDto[] = [];

while (true) {
  const { data: result } = await documents.documentsControllerListDocuments(page, limit);
  allDocuments.push(...result.data);
  if (allDocuments.length >= result.pagination.total) break;
  page++;
}
```

---

## Error Handling

API errors are returned as `AxiosError` responses. The response body typically follows the `ErrorDto` shape:

```typescript
import { AxiosError } from 'axios';

try {
  await documents.documentsControllerGetDocument('nonexistent-id');
} catch (err) {
  if (err instanceof AxiosError && err.response) {
    const error = err.response.data as ErrorDto;
    console.error(`[${err.response.status}] ${error.error}: ${error.message}`);
    // error.requestId — use for support/tracking
    // error.details   — additional context
  }
}
```

Validation errors (HTTP 422) include granular issue details:

```typescript
// ValidationErrorDto
{
  error: 'validation_error',
  message: 'YAML validation failed',
  issues: [
    { path: '/queries/0/question', message: 'Required field missing', severity: 'error' },
    { path: '/options/model', message: 'Unknown model name', severity: 'warning' },
  ],
  requestId: '...'
}
```

---

## Models Reference

| Model | Description |
|-------|-------------|
| `ProfileDto` | Processing profile/config with name, description, YAML content, and tags |
| `DocumentDto` | Uploaded document with status, file metadata, processing metrics, and tags |
| `DocumentCreateResponseDto` | Response from document creation — contains the `DocumentDto` and initial `JobDto` |
| `JobDto` | Full job details including type, state, progress, stage, and links |
| `JobStatusDto` | Lightweight job status for polling (state, progress, stage, message) |
| `JobLinksDto` | Hypermedia links on a job (status URL, resource URL) |
| `EvalDto` | Evaluation result with status, summary metrics, and detailed report |
| `EvalCreateResponseDto` | Response from eval creation — contains `EvalDto` and `JobDto` |
| `BatchQueryDto` | Batch query with status and optional stored results |
| `QueryCreateResponseDto` | Response from query creation — contains `BatchQueryDto` and `JobDto` |
| `SourceItemDto` | Individual source chunk with text, page number, and metadata |
| `DocumentSourcesResponseDto` | Wrapper around an array of `SourceItemDto` |
| `WebhookDto` | Registered webhook with URL and timestamps |
| `CreateWebhookInputDto` | Input for creating a webhook (`{ url: string }`) |
| `UpdateWebhookBodyInputDto` | Input for updating a webhook (`{ url: string }`) |
| `HealthResponseDto` | System health with overall status and per-component checks |
| `HealthChecksDto` | Individual checks for Redis, DB, and GPU |
| `HealthCheckItemDto` | Single health check with status, latency, and message |
| `GpuHealthCheckDto` | GPU-specific health with device count and per-device info |
| `GpuDeviceDto` | Individual GPU device (name, memory, utilization) |
| `PaginationDto` | Pagination metadata (`page`, `limit`, `total`) |
| `ErrorDto` | Standard error response with error type, message, and request ID |
| `ValidationResultDto` | YAML validation result (`valid`, `warnings`, `normalized`) |
| `ValidationErrorDto` | Validation failure with detailed issues |
| `ValidationIssueDto` | Single validation issue with JSON-pointer path, message, and severity |
| `PaginatedDocumentsDto` | Paginated list of `DocumentDto` |
| `PaginatedEvalsDto` | Paginated list of `EvalDto` |
| `PaginatedJobsDto` | Paginated list of `JobDto` |
| `PaginatedProfilesDto` | Paginated list of `ProfileDto` |
| `PaginatedQueriesDto` | Paginated list of `BatchQueryDto` |
| `PaginatedWebhooksDto` | Paginated list of `WebhookDto` |
