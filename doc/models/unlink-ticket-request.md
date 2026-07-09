
# Unlink Ticket Request

Unlink ticket request

*This model accepts additional fields of type unknown.*

## Structure

`UnlinkTicketRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Required | Deployment ID. Can be found at /deployments, or in your Settings in the web UI. |
| `issueIds` | `string[]` | Required | An array of Semgrep finding IDs to unlink tickets from. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { UnlinkTicketRequest } from 'apimatic-semgrep-sdk';

const unlinkTicketRequest: UnlinkTicketRequest = {
  deploymentId: '123',
  issueIds: [
    'issue_ids2',
    'issue_ids1'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

