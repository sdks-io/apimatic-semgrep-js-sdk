
# Protos Ai V1 Autotriage

*This model accepts additional fields of type unknown.*

## Structure

`ProtosAiV1Autotriage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feedback` | [`ProtosAiV1AutotriageFeedback \| undefined`](../../doc/models/protos-ai-v1-autotriage-feedback.md) | Optional | - |
| `id` | `string \| undefined` | Optional | - |
| `issueId` | `string \| undefined` | Optional | - |
| `matchBasedId` | `string \| undefined` | Optional | - |
| `memoryIdsReferenced` | `string[] \| undefined` | Optional | - |
| `memoryIdsRendered` | `string[] \| undefined` | Optional | - |
| `reason` | `string \| undefined` | Optional | The reasoning for a false positive verdict, explaining why you might want to ignore the finding. Empty string if verdict is true positive. |
| `verdict` | [`Verdict \| undefined`](../../doc/models/verdict.md) | Optional | \| value \| description \|<br>\|-------\|---------------\|<br>\| VERDICT_TRUE_POSITIVE \|  \|<br>\| VERDICT_FALSE_POSITIVE \|  \|<br>\| VERDICT_NO_VERDICT \|  \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosAiV1Autotriage, Rating } from 'apimatic-semgrep-sdk';

const protosAiV1Autotriage: ProtosAiV1Autotriage = {
  feedback: {
    autotriageId: 'autotriageId0',
    note: 'note2',
    rating: Rating.RatingGood,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  id: 'id0',
  issueId: 'issueId8',
  matchBasedId: 'matchBasedId2',
  memoryIdsReferenced: [
    'memoryIdsReferenced2'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

