
# Protos Ticketing V1 External Ticket

*This model accepts additional fields of type unknown.*

## Structure

`ProtosTicketingV1ExternalTicket`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalSlug` | `string \| undefined` | Optional | Identifier of the external ticket (e.g. for Jira, something like OPS-158). |
| `id` | `string \| undefined` | Optional | Nango ticket id |
| `linkedIssueIds` | `string[] \| undefined` | Optional | Semgrep issue ids that are linked to this external ticket |
| `url` | `string \| undefined` | Optional | URL of the external ticket. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosTicketingV1ExternalTicket } from 'apimatic-semgrep-sdk';

const protosTicketingV1ExternalTicket: ProtosTicketingV1ExternalTicket = {
  externalSlug: 'externalSlug6',
  id: 'id6',
  linkedIssueIds: [
    'linkedIssueIds7'
  ],
  url: 'url0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

