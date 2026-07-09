
# Protos Openapi V1 Search Scans Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1SearchScansResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Cursor to retrieve the next page of results. |
| `scans` | [`ProtosScanV1ScanPublic[] \| undefined`](../../doc/models/protos-scan-v1-scan-public.md) | Optional | List of scans. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1SearchScansResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1SearchScansResponse: ProtosOpenapiV1SearchScansResponse = {
  cursor: 'cursor8',
  scans: [
    {
      branch: 'branch6',
      commit: 'commit2',
      completedAt: '2016-03-13T12:52:32.123Z',
      deploymentId: 'deployment_id4',
      enabledProducts: [
        'enabled_products6',
        'enabled_products7'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      branch: 'branch6',
      commit: 'commit2',
      completedAt: '2016-03-13T12:52:32.123Z',
      deploymentId: 'deployment_id4',
      enabledProducts: [
        'enabled_products6',
        'enabled_products7'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

