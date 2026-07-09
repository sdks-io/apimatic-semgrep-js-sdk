
# Protos Ai V1 Autotriage Feedback

*This model accepts additional fields of type unknown.*

## Structure

`ProtosAiV1AutotriageFeedback`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autotriageId` | `string \| undefined` | Optional | - |
| `note` | `string \| undefined` | Optional | - |
| `rating` | [`Rating \| undefined`](../../doc/models/rating.md) | Optional | \| value \| description \|<br>\|-------\|---------------\|<br>\| RATING_GOOD \| Autotriage rated positively by a user. \|<br>\| RATING_BAD \| Autotriage rated negatively by a user. \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosAiV1AutotriageFeedback, Rating } from 'apimatic-semgrep-sdk';

const protosAiV1AutotriageFeedback: ProtosAiV1AutotriageFeedback = {
  autotriageId: 'autotriageId4',
  note: 'note4',
  rating: Rating.RatingGood,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

