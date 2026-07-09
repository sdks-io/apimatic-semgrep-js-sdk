# Projects Service

```ts
const projectsServiceApi = new ProjectsServiceApi(client);
```

## Class Name

`ProjectsServiceApi`

## Methods

* [List Projects](../../doc/controllers/projects-service.md#list-projects)
* [Delete Project](../../doc/controllers/projects-service.md#delete-project)
* [Get Project](../../doc/controllers/projects-service.md#get-project)
* [Update Project](../../doc/controllers/projects-service.md#update-project)
* [Toggle Project Managed Scan](../../doc/controllers/projects-service.md#toggle-project-managed-scan)
* [Delete Project Tags](../../doc/controllers/projects-service.md#delete-project-tags)
* [Add Project Tags](../../doc/controllers/projects-service.md#add-project-tags)


# List Projects

Request the list of projects that have been scanned or onboarded to Managed Scans. Does not return archived repositories. Returns 100 projects per page by default.

```ts
async listProjects(
  deploymentSlug: string,
  page?: bigint,
  pageSize?: bigint,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ListProjectsResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `page` | `bigint \| undefined` | Query, Optional | - |
| `pageSize` | `bigint \| undefined` | Query, Optional | **Default**: `100` |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ListProjectsResponse`](../../doc/models/list-projects-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const page = BigInt(1);

const pageSize = BigInt(100);

try {
  const response = await projectsServiceApi.listProjects(
    deploymentSlug,
    page,
    pageSize
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


# Delete Project

Delete a project for a deployment you have access to. This will also delete all of the associated findings.

```ts
async deleteProject(
  deploymentSlug: string,
  projectName: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<DeleteProjectResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DeleteProjectResponse`](../../doc/models/delete-project-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const projectName = 'organization/project';

try {
  const response = await projectsServiceApi.deleteProject(
    deploymentSlug,
    projectName
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


# Get Project

Retrieve details for a single project associated with a deployment that you have access to.

```ts
async getProject(
  deploymentSlug: string,
  projectName: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<GetProjectResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`GetProjectResponse`](../../doc/models/get-project-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const projectName = 'organization/project';

try {
  const response = await projectsServiceApi.getProject(
    deploymentSlug,
    projectName
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


# Update Project

Update attributes for the project using the value passed in to the request body.

Note: The only attribute that is supported as of January 2023 is `tags`.

```ts
async updateProject(
  deploymentSlug: string,
  projectName: string,
  body: UpdateProjectRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<UpdateProjectResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `body` | [`UpdateProjectRequest`](../../doc/models/update-project-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`UpdateProjectResponse`](../../doc/models/update-project-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const projectName = 'organization/project';

const body: UpdateProjectRequest = {
  deploymentSlug: 'your-deployment',
  projectName: 'organization/project',
  primaryBranch: 'refs/heads/develop',
  tags: [
    'tag'
  ],
};

try {
  const response = await projectsServiceApi.updateProject(
    deploymentSlug,
    projectName,
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


# Toggle Project Managed Scan

Enable or disable
[Semgrep Managed Scans](/docs/deployment/managed-scanning/overview)
for a project.

```ts
async toggleProjectManagedScan(
  deploymentSlug: string,
  projectName: string,
  body: ToggleProjectManagedScanRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ToggleProjectManagedScanResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `body` | [`ToggleProjectManagedScanRequest`](../../doc/models/toggle-project-managed-scan-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ToggleProjectManagedScanResponse`](../../doc/models/toggle-project-managed-scan-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const projectName = 'organization/project';

const body: ToggleProjectManagedScanRequest = {
  deploymentSlug: 'your-deployment',
  projectName: 'organization/project',
};

try {
  const response = await projectsServiceApi.toggleProjectManagedScan(
    deploymentSlug,
    projectName,
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


# Delete Project Tags

Remove tags from a project for a deployment you have access to.

This request will not delete project tags from the deployment and will only remove
them from the requested project. Any other projects associated with the requested
tag will remain unaffected.

```ts
async deleteProjectTags(
  deploymentSlug: string,
  projectName: string,
  tags?: string[],
  requestOptions?: RequestOptions
): Promise<ApiResponse<DeleteProjectTagsResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `tags` | `string[] \| undefined` | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`DeleteProjectTagsResponse`](../../doc/models/delete-project-tags-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const projectName = 'organization/project';

const tags: string[] = [
  'tag'
];

try {
  const response = await projectsServiceApi.deleteProjectTags(
    deploymentSlug,
    projectName,
    tags
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


# Add Project Tags

Add tags to a project for a deployment you have access to.

Any project tags that do not already exist for the deployment will be created automatically and associated with the project.

```ts
async addProjectTags(
  deploymentSlug: string,
  projectName: string,
  body: AddProjectTagsRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<AddProjectTagsResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `projectName` | `string` | Template, Required | - |
| `body` | [`AddProjectTagsRequest`](../../doc/models/add-project-tags-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`AddProjectTagsResponse`](../../doc/models/add-project-tags-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const projectName = 'organization/project';

const body: AddProjectTagsRequest = {
  deploymentSlug: 'your-deployment',
  projectName: 'organization/project',
  tags: [
    'tag'
  ],
};

try {
  const response = await projectsServiceApi.addProjectTags(
    deploymentSlug,
    projectName,
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

