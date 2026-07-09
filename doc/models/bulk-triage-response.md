
# Bulk Triage Response

*This model accepts additional fields of type unknown.*

## Structure

`BulkTriageResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `numTriaged` | `bigint` | Required | Number of items updated |
| `triagedIssues` | `bigint[]` | Required | List of triaged issue IDs |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { BulkTriageResponse } from 'apimatic-semgrep-sdk';

const bulkTriageResponse: BulkTriageResponse = {
  numTriaged: BigInt(232),
  triagedIssues: [
    BigInt(68),
    BigInt(69),
    BigInt(70)
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

