
# Protos Openapi V1 Diff Scan

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1DiffScan`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean \| undefined` | Optional | When true, diff-aware scans are enabled for the project. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1DiffScan } from 'apimatic-semgrep-sdk';

const protosOpenapiV1DiffScan: ProtosOpenapiV1DiffScan = {
  enabled: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

