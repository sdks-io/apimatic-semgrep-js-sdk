
# Finding Location

Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans)

*This model accepts additional fields of type unknown.*

## Structure

`FindingLocation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `column` | `bigint \| undefined` | Optional | Column at which the target starts |
| `endColumn` | `bigint \| undefined` | Optional | Column at which the target ends |
| `endLine` | `bigint \| undefined` | Optional | Line at which the target ends |
| `filePath` | `string \| undefined` | Optional | File path of the relevant line and column numbers |
| `line` | `bigint \| undefined` | Optional | Line at which the target starts |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { FindingLocation } from 'apimatic-semgrep-sdk';

const findingLocation: FindingLocation = {
  column: BigInt(8),
  endColumn: BigInt(16),
  endLine: BigInt(124),
  filePath: 'frontend/src/corpComponents/Code.tsx',
  line: BigInt(120),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

