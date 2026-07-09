
# Protos Sca V1 Code Location

Specific location in a file.

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1CodeLocation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `committedAt` | `string \| undefined` | Optional | Timestamp when code file was last modified, if available. |
| `endCol` | `string \| undefined` | Optional | Ending column number (1 indexed). |
| `endLine` | `string \| undefined` | Optional | Ending line number (1 indexed). |
| `path` | `string \| undefined` | Optional | Path to a file. |
| `startCol` | `string \| undefined` | Optional | Starting column number (1 indexed). |
| `startLine` | `string \| undefined` | Optional | Starting line number (1 indexed). |
| `url` | `string \| undefined` | Optional | URL to code location if available, otherwise empty. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1CodeLocation } from 'apimatic-semgrep-sdk';

const protosScaV1CodeLocation: ProtosScaV1CodeLocation = {
  committedAt: '2016-03-13T12:52:32.123Z',
  endCol: 'endCol6',
  endLine: 'endLine0',
  path: 'path0',
  startCol: 'startCol0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

