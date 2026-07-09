
# Protos Openapi V1 List Secrets Path Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1ListSecretsPathResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Cursor to paginate through the results. |
| `findings` | [`ProtosSecretsV1SecretsFinding[] \| undefined`](../../doc/models/protos-secrets-v1-secrets-finding.md) | Optional | List of Secrets associated with the given Deployment. |
| `previous` | `string \| undefined` | Optional | Cursor to paginate backwards through the results. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence7,
  ProtosOpenapiV1ListSecretsPathResponse,
  Rating,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1ListSecretsPathResponse: ProtosOpenapiV1ListSecretsPathResponse = {
  cursor: 'cursor4',
  findings: [
    {
      autotriage: {
        feedback: {
          autotriageId: 'autotriageId0',
          note: 'note2',
          rating: Rating.RatingGood,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        id: 'id2',
        issueId: 'issueId0',
        matchBasedId: 'matchBasedId6',
        memoryIdsReferenced: [
          'memoryIdsReferenced4'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      confidence: Confidence7.ConfidenceHigh,
      createdAt: '2016-03-13T12:52:32.123Z',
      externalTicket: {
        externalSlug: 'externalSlug6',
        id: 'id6',
        linkedIssueIds: [
          'linkedIssueIds7'
        ],
        url: 'url0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      findingPath: 'findingPath8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      autotriage: {
        feedback: {
          autotriageId: 'autotriageId0',
          note: 'note2',
          rating: Rating.RatingGood,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        id: 'id2',
        issueId: 'issueId0',
        matchBasedId: 'matchBasedId6',
        memoryIdsReferenced: [
          'memoryIdsReferenced4'
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      confidence: Confidence7.ConfidenceHigh,
      createdAt: '2016-03-13T12:52:32.123Z',
      externalTicket: {
        externalSlug: 'externalSlug6',
        id: 'id6',
        linkedIssueIds: [
          'linkedIssueIds7'
        ],
        url: 'url0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      findingPath: 'findingPath8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  previous: 'previous0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

