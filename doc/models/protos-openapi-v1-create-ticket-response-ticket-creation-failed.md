
# Protos Openapi V1 Create Ticket Response Ticket Creation Failed

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1CreateTicketResponseTicketCreationFailed`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error` | `string \| undefined` | Optional | The error message for the failure |
| `issueIds` | `bigint[] \| undefined` | Optional | List of issue IDs |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ProtosOpenapiV1CreateTicketResponseTicketCreationFailed,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1CreateTicketResponseTicketCreationFailed: ProtosOpenapiV1CreateTicketResponseTicketCreationFailed = {
  error: 'error8',
  issueIds: [
    BigInt(36),
    BigInt(37)
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

