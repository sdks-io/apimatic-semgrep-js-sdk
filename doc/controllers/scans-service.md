# Scans Service

View details of scans associated with projects in your organization.

```ts
const scansServiceApi = new ScansServiceApi(client);
```

## Class Name

`ScansServiceApi`

## Methods

* [Get Scan](../../doc/controllers/scans-service.md#get-scan)
* [Search Scans](../../doc/controllers/scans-service.md#search-scans)


# Get Scan

Request the details of a scan including the associated deployment, repository, and commit information.

```ts
async getScan(
  deploymentId: string,
  scanId: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1GetScanResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `scanId` | `string` | Template, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1GetScanResponse`](../../doc/models/protos-openapi-v1-get-scan-response.md).

## Example Usage

```ts
const deploymentId = '123';

const scanId = '456';

try {
  const response = await scansServiceApi.getScan(
    deploymentId,
    scanId
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


# Search Scans

List the scans associated with a particular repository over the past 30 days.

```ts
async searchScans(
  deploymentId: string,
  body: SearchScansRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1SearchScansResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`SearchScansRequest`](../../doc/models/search-scans-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1SearchScansResponse`](../../doc/models/protos-openapi-v1-search-scans-response.md).

## Example Usage

```ts
const deploymentId = '123';

const body: SearchScansRequest = {
  deploymentId: '123',
};

try {
  const response = await scansServiceApi.searchScans(
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

