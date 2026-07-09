# Secrets Service

View and manage the Secrets of your organization.

```ts
const secretsServiceApi = new SecretsServiceApi(client);
```

## Class Name

`SecretsServiceApi`


# List Secrets Path

```ts
async listSecretsPath(
  deploymentId: string,
  cursor?: string,
  limit?: bigint,
  since?: string,
  validationState?: ValidationState3[],
  status?: Status8,
  severity?: Severity5[],
  repo?: string[],
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1ListSecretsPathResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `cursor` | `string \| undefined` | Query, Optional | - |
| `limit` | `bigint \| undefined` | Query, Optional | - |
| `since` | `string \| undefined` | Query, Optional | - |
| `validationState` | [`ValidationState3[] \| undefined`](../../doc/models/validation-state-3.md) | Query, Optional | - |
| `status` | [`Status8 \| undefined`](../../doc/models/status-8.md) | Query, Optional | **Default**: `Status8.FindingStatusUnspecified` |
| `severity` | [`Severity5[] \| undefined`](../../doc/models/severity-5.md) | Query, Optional | - |
| `repo` | `string[] \| undefined` | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1ListSecretsPathResponse`](../../doc/models/protos-openapi-v1-list-secrets-path-response.md).

## Example Usage

```ts
const deploymentId = '123';

const status = Status8.FindingStatusUnspecified;

try {
  const response = await secretsServiceApi.listSecretsPath(
    deploymentId,
    undefined,
    undefined,
    undefined,
    undefined,
    status
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

