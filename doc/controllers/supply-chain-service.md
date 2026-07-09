# Supply Chain Service

Manage the Supply Chain findings and dependencies of your organization.

A request body is required, but may be an empty object.

```ts
const supplyChainServiceApi = new SupplyChainServiceApi(client);
```

## Class Name

`SupplyChainServiceApi`

## Methods

* [List Dependencies](../../doc/controllers/supply-chain-service.md#list-dependencies)
* [List Repositories for Dependencies](../../doc/controllers/supply-chain-service.md#list-repositories-for-dependencies)
* [List Lockfiles for Dependencies](../../doc/controllers/supply-chain-service.md#list-lockfiles-for-dependencies)
* [Create Sbom Export](../../doc/controllers/supply-chain-service.md#create-sbom-export)
* [Get Sbom Export](../../doc/controllers/supply-chain-service.md#get-sbom-export)


# List Dependencies

```ts
async listDependencies(
  deploymentId: string,
  body: ListDependenciesRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ListDependenciesResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`ListDependenciesRequest`](../../doc/models/list-dependencies-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ListDependenciesResponse`](../../doc/models/list-dependencies-response.md).

## Example Usage

```ts
const deploymentId = '123';

const body: ListDependenciesRequest = {
  deploymentId: '123',
  pageSize: BigInt(1000),
};

try {
  const response = await supplyChainServiceApi.listDependencies(
    deploymentId,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# List Repositories for Dependencies

```ts
async listRepositoriesForDependencies(
  deploymentId: string,
  body: ListRepositoriesForDependenciesRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ListRepositoriesForDependenciesResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`ListRepositoriesForDependenciesRequest`](../../doc/models/list-repositories-for-dependencies-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ListRepositoriesForDependenciesResponse`](../../doc/models/list-repositories-for-dependencies-response.md).

## Example Usage

```ts
const deploymentId = 'deploymentId2';

const body: ListRepositoriesForDependenciesRequest = {
  deploymentId: 'deploymentId8',
  pageSize: BigInt(100),
};

try {
  const response = await supplyChainServiceApi.listRepositoriesForDependencies(
    deploymentId,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# List Lockfiles for Dependencies

```ts
async listLockfilesForDependencies(
  deploymentId: string,
  repositoryId: string,
  body: ListLockfilesForDependenciesRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ListLockfilesForDependenciesResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `repositoryId` | `string` | Template, Required | - |
| `body` | [`ListLockfilesForDependenciesRequest`](../../doc/models/list-lockfiles-for-dependencies-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ListLockfilesForDependenciesResponse`](../../doc/models/list-lockfiles-for-dependencies-response.md).

## Example Usage

```ts
const deploymentId = 'deploymentId2';

const repositoryId = 'repositoryId6';

const body: ListLockfilesForDependenciesRequest = {
  deploymentId: 'deploymentId8',
  repositoryId: 'repositoryId0',
  pageSize: BigInt(100),
};

try {
  const response = await supplyChainServiceApi.listLockfilesForDependencies(
    deploymentId,
    repositoryId,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# Create Sbom Export

```ts
async createSbomExport(
  deploymentId: string,
  body: CreateSbomExportRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<CreateSbomExportResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`CreateSbomExportRequest`](../../doc/models/create-sbom-export-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CreateSbomExportResponse`](../../doc/models/create-sbom-export-response.md).

## Example Usage

```ts
const deploymentId = '123';

const body: CreateSbomExportRequest = {
  deploymentId: '123',
  metadataComponentType: MetadataComponentType.SbomMetadataComponentTypeCycloneDxV15Application,
  ref: 'refs/pull/1234/merge',
  repositoryId: '123',
  sbomOutputFormat: SbomOutputFormat.SbomOutputFormatJson,
};

try {
  const response = await supplyChainServiceApi.createSbomExport(
    deploymentId,
    body
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```


# Get Sbom Export

```ts
async getSbomExport(
  deploymentId: string,
  taskToken: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<GetSbomExportResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `taskToken` | `string` | Template, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`GetSbomExportResponse`](../../doc/models/get-sbom-export-response.md).

## Example Usage

```ts
const deploymentId = '123';

const taskToken = 'taskToken2';

try {
  const response = await supplyChainServiceApi.getSbomExport(
    deploymentId,
    taskToken
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

