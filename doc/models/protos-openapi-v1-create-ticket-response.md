
# Protos Openapi V1 Create Ticket Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1CreateTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `failed` | [`ProtosOpenapiV1CreateTicketResponseTicketCreationFailed[] \| undefined`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-failed.md) | Optional | List of issues where ticket creation failed. This list may include issues that were skipped because they exceed the specified limit. |
| `skipped` | [`ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped[] \| undefined`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-skipped.md) | Optional | List of issues that were skipped |
| `succeeded` | [`ProtosOpenapiV1CreateTicketResponseTicketCreationSuccess[] \| undefined`](../../doc/models/protos-openapi-v1-create-ticket-response-ticket-creation-success.md) | Optional | List of successfully created tickets |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1CreateTicketResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1CreateTicketResponse: ProtosOpenapiV1CreateTicketResponse = {
  failed: [
    {
      error: 'error6',
      issueIds: [
        BigInt(196)
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      error: 'error6',
      issueIds: [
        BigInt(196)
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  skipped: [
    {
      issueIds: [
        BigInt(38)
      ],
      reason: 'reason4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      issueIds: [
        BigInt(38)
      ],
      reason: 'reason4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  succeeded: [
    {
      externalSlug: 'external_slug4',
      issueIds: [
        BigInt(230),
        BigInt(229),
        BigInt(228)
      ],
      ticketId: BigInt(2),
      ticketUrl: 'ticket_url0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      externalSlug: 'external_slug4',
      issueIds: [
        BigInt(230),
        BigInt(229),
        BigInt(228)
      ],
      ticketId: BigInt(2),
      ticketUrl: 'ticket_url0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      externalSlug: 'external_slug4',
      issueIds: [
        BigInt(230),
        BigInt(229),
        BigInt(228)
      ],
      ticketId: BigInt(2),
      ticketUrl: 'ticket_url0',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

