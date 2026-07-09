
# Link Ticket Request

Link ticket request

*This model accepts additional fields of type unknown.*

## Structure

`LinkTicketRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Required | Deployment ID. Can be found at /deployments, or in your Settings in the web UI. |
| `issueIds` | `string[]` | Required | An array of Semgrep finding IDs to link the ticket to. |
| `ticketUrl` | `string` | Required | The URL of the external ticket to link (e.g. https://myorg.atlassian.net/browse/SEC-123). |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { LinkTicketRequest } from 'apimatic-semgrep-sdk';

const linkTicketRequest: LinkTicketRequest = {
  deploymentId: '123',
  issueIds: [
    'issue_ids4',
    'issue_ids5'
  ],
  ticketUrl: 'https://myorg.atlassian.net/browse/SEC-123',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

