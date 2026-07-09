
# Protos Openapi V1 Delete Ticket Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1DeleteTicketResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `issueIds` | `string[] \| undefined` | Optional | List of issue IDs unlinked from ticket |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1DeleteTicketResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1DeleteTicketResponse: ProtosOpenapiV1DeleteTicketResponse = {
  issueIds: [
    '18759',
    '18760'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

