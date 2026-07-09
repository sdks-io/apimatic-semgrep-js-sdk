
# Managed Scan Config

[Beta] Configuration of Semgrep Managed Scans for the project, if relevant.

*This model accepts additional fields of type unknown.*

## Structure

`ManagedScanConfig`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `diffScan` | [`ProtosOpenapiV1DiffScan \| undefined`](../../doc/models/protos-openapi-v1-diff-scan.md) | Optional | - |
| `fullScan` | [`ProtosOpenapiV1FullScan \| undefined`](../../doc/models/protos-openapi-v1-full-scan.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ManagedScanConfig } from 'apimatic-semgrep-sdk';

const managedScanConfig: ManagedScanConfig = {
  diffScan: {
    enabled: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  fullScan: {
    enabled: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

