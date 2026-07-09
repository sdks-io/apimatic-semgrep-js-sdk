
# External Ticket

External ticket associated with finding

*This model accepts additional fields of type unknown.*

## Structure

`ExternalTicket`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalSlug` | `string \| undefined` | Optional | Identifier of the external ticket |
| `id` | `bigint \| undefined` | Optional | External ticket id |
| `linkedIssueIds` | `bigint[] \| undefined` | Optional | Semgrep issue ids that are linked to this external ticket |
| `url` | `string \| undefined` | Optional | URL of the external ticket |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ExternalTicket } from 'apimatic-semgrep-sdk';

const externalTicket: ExternalTicket = {
  externalSlug: 'OPS-158',
  id: BigInt(74),
  linkedIssueIds: [
    BigInt(217),
    BigInt(218)
  ],
  url: 'url0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

