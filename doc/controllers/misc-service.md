# Misc Service

Utility endpoints.

```ts
const miscServiceApi = new MiscServiceApi(client);
```

## Class Name

`MiscServiceApi`

## Methods

* [Get Bootstrap Sms Vpc](../../doc/controllers/misc-service.md#get-bootstrap-sms-vpc)
* [Ping](../../doc/controllers/misc-service.md#ping)


# Get Bootstrap Sms Vpc

VPC support for Managed Scans is in private beta.

Returns the Managed Scans VPC Bootstrap CloudFormation template in JSON format for setting up cross-account infrastructure.

This template creates IAM roles and policies needed for Semgrep Managed Scanning (SMS) VPC infrastructure automation,
including the semgrep-sms-vpc-automation role and EC2 Image Builder distribution roles for gVisor container runtime.

See the original AWS cloudformation template format at https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html

:information_source: **Note** This endpoint does not require authentication.

```ts
async getBootstrapSmsVpc(
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1GetBootstrapSmsVpcResponse>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1GetBootstrapSmsVpcResponse`](../../doc/models/protos-openapi-v1-get-bootstrap-sms-vpc-response.md).

## Example Usage

```ts
try {
  const response = await miscServiceApi.getBootstrapSmsVpc();

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


# Ping

Use to ping the server and assert liveness.

:information_source: **Note** This endpoint does not require authentication.

```ts
async ping(
  requestOptions?: RequestOptions
): Promise<ApiResponse<unknown | undefined>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type `unknown`.

## Example Usage

```ts
try {
  const response = await miscServiceApi.ping();

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

