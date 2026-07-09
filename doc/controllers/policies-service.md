# Policies Service

View and manage the Policies of your organization.

```ts
const policiesServiceApi = new PoliciesServiceApi(client);
```

## Class Name

`PoliciesServiceApi`

## Methods

* [List Policies](../../doc/controllers/policies-service.md#list-policies)
* [List Policy Rules](../../doc/controllers/policies-service.md#list-policy-rules)
* [Update Policy](../../doc/controllers/policies-service.md#update-policy)


# List Policies

```ts
async listPolicies(
  deploymentId: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1ListPoliciesResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1ListPoliciesResponse`](../../doc/models/protos-openapi-v1-list-policies-response.md).

## Example Usage

```ts
const deploymentId = '123';

try {
  const response = await policiesServiceApi.listPolicies(deploymentId);

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


# List Policy Rules

```ts
async listPolicyRules(
  deploymentId: string,
  policyId: string,
  cursor?: string,
  limit?: bigint,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1ListPolicyRulesResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `policyId` | `string` | Template, Required | - |
| `cursor` | `string \| undefined` | Query, Optional | - |
| `limit` | `bigint \| undefined` | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1ListPolicyRulesResponse`](../../doc/models/protos-openapi-v1-list-policy-rules-response.md).

## Example Usage

```ts
const deploymentId = '123';

const policyId = '456';

try {
  const response = await policiesServiceApi.listPolicyRules(
    deploymentId,
    policyId
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


# Update Policy

```ts
async updatePolicy(
  deploymentId: string,
  policyId: string,
  body: UpdatePolicyRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1UpdatePolicyResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `policyId` | `string` | Template, Required | - |
| `body` | [`UpdatePolicyRequest`](../../doc/models/update-policy-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1UpdatePolicyResponse`](../../doc/models/protos-openapi-v1-update-policy-response.md).

## Example Usage

```ts
const deploymentId = '123';

const policyId = '456';

const body: UpdatePolicyRequest = {
  deploymentId: '123',
  policyId: '456',
  policyMode: PolicyMode3.ModeBlock,
  rulePath: 'rulePath2',
};

try {
  const response = await policiesServiceApi.updatePolicy(
    deploymentId,
    policyId,
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

