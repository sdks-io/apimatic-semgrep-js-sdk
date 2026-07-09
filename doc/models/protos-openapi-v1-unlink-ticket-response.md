
# Protos Openapi V1 Unlink Ticket Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1UnlinkTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `unlinkedIssueIds` | `string[] \| undefined` | Optional | List of finding IDs that were successfully unlinked from their tickets |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1UnlinkTicketResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1UnlinkTicketResponse: ProtosOpenapiV1UnlinkTicketResponse = {
  unlinkedIssueIds: [
    'unlinked_issue_ids6',
    'unlinked_issue_ids7',
    'unlinked_issue_ids8'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

