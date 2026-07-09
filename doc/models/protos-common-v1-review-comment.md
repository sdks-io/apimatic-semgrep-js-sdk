
# Protos Common V1 Review Comment

*This model accepts additional fields of type unknown.*

## Structure

`ProtosCommonV1ReviewComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalDiscussionId` | `string \| undefined` | Optional | External ID of the review comment or discussion thread. |
| `externalNoteId` | `string \| undefined` | Optional | External ID of the specific note in the review comment discussion thread. Only applicable for GitLab.com, GitLab Self-Managed and Azure DevOps. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosCommonV1ReviewComment } from 'apimatic-semgrep-sdk';

const protosCommonV1ReviewComment: ProtosCommonV1ReviewComment = {
  externalDiscussionId: 'externalDiscussionId8',
  externalNoteId: 'externalNoteId0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

