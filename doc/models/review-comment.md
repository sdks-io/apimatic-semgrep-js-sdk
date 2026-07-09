
# Review Comment

External review comment information associated with a finding

*This model accepts additional fields of type unknown.*

## Structure

`ReviewComment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `externalDiscussionId` | `string \| undefined` | Optional | External ID of the review comment or discussion thread |
| `externalNoteId` | `string \| undefined` | Optional | External ID of the specific note in the review comment discussion thread. Only applicable for GitLab.com, GitLab Self-Managed and Azure DevOps |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ReviewComment } from 'apimatic-semgrep-sdk';

const reviewComment: ReviewComment = {
  externalDiscussionId: 'af04762b69acfb74c8f9',
  externalNoteId: '123523',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

