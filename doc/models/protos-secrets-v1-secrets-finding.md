
# Protos Secrets V1 Secrets Finding

A Finding represents a single secret finding.

*This model accepts additional fields of type unknown.*

## Structure

`ProtosSecretsV1SecretsFinding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autotriage` | [`ProtosAiV1Autotriage \| undefined`](../../doc/models/protos-ai-v1-autotriage.md) | Optional | * Autotriage info for the finding.<br>  This is used for the Generic Secrets Detection project, for<br>  autotriaging secrets findings with LLMs |
| `confidence` | [`Confidence7 \| undefined`](../../doc/models/confidence-7.md) | Optional | Confidence of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| CONFIDENCE_HIGH \|  \|<br>\| CONFIDENCE_MEDIUM \|  \|<br>\| CONFIDENCE_LOW \|  \| |
| `createdAt` | `string \| undefined` | Optional | Creation timestamp. |
| `externalTicket` | [`ProtosTicketingV1ExternalTicket \| undefined`](../../doc/models/protos-ticketing-v1-external-ticket.md) | Optional | The external ticket reference |
| `findingPath` | `string \| undefined` | Optional | File path where the finding was detected. |
| `findingPathUrl` | `string \| undefined` | Optional | URL to the file where the finding was detected. |
| `historicalInfo` | [`ProtosSecretsV1HistoricalInfo \| undefined`](../../doc/models/protos-secrets-v1-historical-info.md) | Optional | Historical scanning info for the finding. |
| `id` | `string \| undefined` | Optional | ID of the finding. |
| `mode` | [`Mode \| undefined`](../../doc/models/mode.md) | Optional | The behavior of the finding reporting: Monitor / Comment / Block.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| |
| `ref` | `string \| undefined` | Optional | Branch where the finding was detected. |
| `refUrl` | `string \| undefined` | Optional | URL to the branch where the finding was detected. |
| `repository` | [`ProtosSecretsV1SecretsFindingRepository \| undefined`](../../doc/models/protos-secrets-v1-secrets-finding-repository.md) | Optional | Repository where the finding was detected. |
| `reviewComments` | [`ProtosCommonV1ReviewComment[] \| undefined`](../../doc/models/protos-common-v1-review-comment.md) | Optional | List of external review comment information associated with a finding |
| `ruleHashId` | `string \| undefined` | Optional | ID of the rule that triggered the finding. |
| `severity` | [`Severity4 \| undefined`](../../doc/models/severity-4.md) | Optional | Severity of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SEVERITY_HIGH \|  \|<br>\| SEVERITY_MEDIUM \|  \|<br>\| SEVERITY_LOW \|  \|<br>\| SEVERITY_CRITICAL \|  \| |
| `status` | [`Status6 \| undefined`](../../doc/models/status-6.md) | Optional | Status of the finding.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| FINDING_STATUS_OPEN \|  \|<br>\| FINDING_STATUS_IGNORED \|  \|<br>\| FINDING_STATUS_FIXED \|  \|<br>\| FINDING_STATUS_REMOVED \|  \|<br>\| FINDING_STATUS_UNKNOWN \|  \|<br>\| FINDING_STATUS_PROVISIONALLY_IGNORED \|  \| |
| `type` | `string \| undefined` | Optional | Service type for the secrets finding (e.g. AWS, GitHub, GitLab, etc). |
| `updatedAt` | `string \| undefined` | Optional | Update timestamp. |
| `validationState` | [`ValidationState2 \| undefined`](../../doc/models/validation-state-2.md) | Optional | Whether the finding was validated or not.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| VALIDATION_STATE_CONFIRMED_VALID \|  \|<br>\| VALIDATION_STATE_CONFIRMED_INVALID \|  \|<br>\| VALIDATION_STATE_VALIDATION_ERROR \|  \|<br>\| VALIDATION_STATE_NO_VALIDATOR \|  \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence7,
  ProtosSecretsV1SecretsFinding,
  Rating,
} from 'apimatic-semgrep-sdk';

const protosSecretsV1SecretsFinding: ProtosSecretsV1SecretsFinding = {
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
  confidence: Confidence7.ConfidenceLow,
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
  findingPath: 'findingPath2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

