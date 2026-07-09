
# Protos Openapi V1 Get Scan Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1GetScanResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completedAt` | `string \| undefined` | Optional | imestamp of when the scan started. |
| `deploymentId` | `bigint \| undefined` | Optional | The unique ID of the deployment associated with the scanned repository. |
| `enabledProducts` | `string[] \| undefined` | Optional | The products used when running the scan. |
| `exitCode` | `bigint \| undefined` | Optional | - |
| `hasLogs` | `boolean \| undefined` | Optional | - |
| `id` | `bigint \| undefined` | Optional | The unique ID representing this scan. |
| `meta` | [`ProtosOpenapiV1GetScanResponseScanMeta \| undefined`](../../doc/models/protos-openapi-v1-get-scan-response-scan-meta.md) | Optional | - |
| `repositoryId` | `bigint \| undefined` | Optional | The unique ID of the repository that was scanned. |
| `startedAt` | `string \| undefined` | Optional | when the scan was started |
| `stats` | `unknown \| undefined` | Optional | Miscellaneous statistics about the scan, like number of findings found and scan duration. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1GetScanResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1GetScanResponse: ProtosOpenapiV1GetScanResponse = {
  completedAt: '2023-11-18 23:28:12.391807+00:00',
  deploymentId: BigInt(120),
  enabledProducts: [
    'secrets'
  ],
  exitCode: BigInt(102),
  hasLogs: false,
  id: BigInt(123),
  repositoryId: BigInt(1234567),
  startedAt: '2023-11-18 23:28:12.391807+00:00',
  stats: { 'findings': 5, 'total_time': 100 },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

