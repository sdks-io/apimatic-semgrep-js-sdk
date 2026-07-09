# Deployments Service

Deployments encapsulate your organization's security organization, with multiple projects, policies, and integrations. As the root object of the organization, they're similarly the root object of the API.

```ts
const deploymentsServiceApi = new DeploymentsServiceApi(client);
```

## Class Name

`DeploymentsServiceApi`


# List Deployments

Request the deployments your auth can access.

Currently available auth scope does not extend over more than one deployment. This endpoint returns the single deployment your token can access. The endpoint additionally returns links to related resources available on this API.

```ts
async listDeployments(
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1ListDeploymentsResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1ListDeploymentsResponse`](../../doc/models/protos-openapi-v1-list-deployments-response.md).

## Example Usage

```ts
try {
  const response = await deploymentsServiceApi.listDeployments();

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

