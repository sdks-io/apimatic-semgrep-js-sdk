
# Usage

Usage of the vulnerable package in the codebase. Applies to reachable findings

*This model accepts additional fields of type unknown.*

## Structure

`Usage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalTicket` | [`ExternalTicket \| undefined`](../../doc/models/external-ticket.md) | Optional | External ticket associated with finding |
| `location` | [`FindingLocation \| undefined`](../../doc/models/finding-location.md) | Optional | Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Usage } from 'apimatic-semgrep-sdk';

const usage: Usage = {
  externalTicket: {
    externalSlug: 'external_slug4',
    id: BigInt(228),
    linkedIssueIds: [
      BigInt(115),
      BigInt(116),
      BigInt(117)
    ],
    url: 'url8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  location: {
    column: BigInt(222),
    endColumn: BigInt(174),
    endLine: BigInt(120),
    filePath: 'file_path0',
    line: BigInt(114),
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

