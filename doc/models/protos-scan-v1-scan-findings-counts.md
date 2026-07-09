
# Protos Scan V1 Scan Findings Counts

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScanV1ScanFindingsCounts`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `string \| undefined` | Optional | Total number of Code findings in the scan |
| `secrets` | `string \| undefined` | Optional | Total number of Secrets findings in the scan |
| `supplyChain` | `string \| undefined` | Optional | Total number of Supply Chain findings in the scan |
| `total` | `string \| undefined` | Optional | Total number of findings in the scan |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScanV1ScanFindingsCounts } from 'apimatic-semgrep-sdk';

const protosScanV1ScanFindingsCounts: ProtosScanV1ScanFindingsCounts = {
  code: '2',
  secrets: '1',
  supplyChain: '1',
  total: '4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

