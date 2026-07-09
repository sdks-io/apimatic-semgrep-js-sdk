
# Protos Openapi V1 Link Ticket Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1LinkTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalSlug` | `string \| undefined` | Optional | The external slug identifier for the ticket (e.g. SEC-123) |
| `linkedIssueIds` | `string[] \| undefined` | Optional | List of finding IDs that were successfully linked to the ticket |
| `replacedIssueIds` | `string[] \| undefined` | Optional | List of finding IDs where an existing ticket link was replaced |
| `ticketId` | `bigint \| undefined` | Optional | The internal ID of the linked ticket record |
| `ticketUrl` | `string \| undefined` | Optional | The URL of the linked ticket |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1LinkTicketResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1LinkTicketResponse: ProtosOpenapiV1LinkTicketResponse = {
  externalSlug: 'external_slug4',
  linkedIssueIds: [
    'linked_issue_ids1'
  ],
  replacedIssueIds: [
    'replaced_issue_ids5'
  ],
  ticketId: BigInt(148),
  ticketUrl: 'ticket_url8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

