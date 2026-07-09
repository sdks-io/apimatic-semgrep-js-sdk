
# Protos Openapi V1 Create Ticket Response Ticket Creation Skipped

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `issueIds` | `bigint[] \| undefined` | Optional | List of issue IDs |
| `reason` | `string \| undefined` | Optional | The reason why the issue was skipped |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1CreateTicketResponseTicketCreationSkipped: ProtosOpenapiV1CreateTicketResponseTicketCreationSkipped = {
  issueIds: [
    BigInt(74),
    BigInt(75)
  ],
  reason: 'reason4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

