
# Protos Openapi V1 Create Ticket Response Ticket Creation Success

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalSlug` | `string \| undefined` | Optional | The external slug identifier for the ticket |
| `issueIds` | `bigint[] \| undefined` | Optional | List of issue IDs |
| `ticketId` | `bigint \| undefined` | Optional | The ID of the created ticket |
| `ticketUrl` | `string \| undefined` | Optional | The URL of the created ticket |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1CreateTicketResponseTicketCreationSuccess: ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess = {
  externalSlug: 'external_slug8',
  issueIds: [
    BigInt(118),
    BigInt(117)
  ],
  ticketId: BigInt(114),
  ticketUrl: 'ticket_url6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

