
# Protos Openapi V1 Full Scan

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1FullScan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean \| undefined` | Optional | When true, weekly full scans are enabled. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1FullScan } from 'apimatic-semgrep-sdk';

const protosOpenapiV1FullScan: ProtosOpenapiV1FullScan = {
  enabled: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

