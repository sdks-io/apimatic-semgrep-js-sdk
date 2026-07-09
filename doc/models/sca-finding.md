
# Sca Finding

A Supply Chain finding that Semgrep has identified in your organization

*This model accepts additional fields of type unknown.*

## Structure

`ScaFinding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categories` | `string[] \| undefined` | Optional | The categories of the finding as classified by the associated rule metadata |
| `confidence` | [`Confidence1 \| undefined`](../../doc/models/confidence-1.md) | Optional | Confidence of the finding, derived from the rule that triggered it |
| `createdAt` | `string \| undefined` | Optional | The timestamp when this finding was created |
| `epssScore` | [`EpssScore \| undefined`](../../doc/models/epss-score.md) | Optional | The score assigned by FIRST.org's Exploitation Probability Scoring System |
| `externalTicket` | [`ExternalTicket \| undefined`](../../doc/models/external-ticket.md) | Optional | External ticket associated with finding |
| `firstSeenScanId` | `bigint \| undefined` | Optional | Unique ID of the Semgrep scan that first identified this finding |
| `fixRecommendations` | [`FixRecommendation[] \| undefined`](../../doc/models/fix-recommendation.md) | Optional | Recommendations for fixing the vulnerability |
| `foundDependency` | [`FoundDependency \| undefined`](../../doc/models/found-dependency.md) | Optional | Information about the vulnerable package that was found in the codebase |
| `id` | `bigint \| undefined` | Optional | Unique ID of this finding |
| `isMalicious` | `boolean \| undefined` | Optional | True if the finding is from a malicious dependency |
| `lineOfCodeUrl` | `string \| undefined` | Optional | The source URL including file and line number |
| `location` | [`FindingLocation \| undefined`](../../doc/models/finding-location.md) | Optional | Location of the record in a file, as reported by Semgrep. If null, then the information does not exist or lacks integrity (older or broken scans) |
| `matchBasedId` | `string \| undefined` | Optional | ID calculated based on a finding's file path, rule identifier and pattern, and index |
| `reachability` | [`Reachability \| undefined`](../../doc/models/reachability.md) | Optional | Indicates whether the vulnerable code is reachable |
| `reachableCondition` | `string \| undefined` | Optional | Description of the condition under which the vulnerability becomes reachable. Applies to conditionally reachable findings |
| `ref` | `string \| undefined` | Optional | External reference to the source of this finding (e.g. PR) |
| `relevantSince` | `string \| undefined` | Optional | The timestamp when this finding was detected by Semgrep (the first time, or when reintroduced) |
| `repository` | [`FindingRepository \| undefined`](../../doc/models/finding-repository.md) | Optional | Which repository this finding was identified in |
| `reviewComments` | [`ReviewComment[] \| undefined`](../../doc/models/review-comment.md) | Optional | List of external review comment information associated with a finding |
| `rule` | [`FindingRule \| undefined`](../../doc/models/finding-rule.md) | Optional | Rule that applies to this finding |
| `ruleMessage` | `string \| undefined` | Optional | Deprecated in favor of rule.message. Rule message at the time of finding identification. Older findings may not have a value for this field |
| `ruleName` | `string \| undefined` | Optional | Deprecated in favor of rule.name |
| `severity` | [`Severity1 \| undefined`](../../doc/models/severity-1.md) | Optional | Severity of the finding, derived from the rule that triggered it. Low is equivalent to INFO, Medium to WARNING, and High to ERROR |
| `state` | [`State \| undefined`](../../doc/models/state.md) | Optional | The finding's resolution state. Managed only by changes detected at scan time, the `state` is combined with `triage_state` to ultimately determine a final `status` which is exposed in the UI and API |
| `stateUpdatedAt` | `string \| undefined` | Optional | When this issue's `state` (resolution state) was last updated, as distinct from when the issue was triaged (`triaged_at`) |
| `status` | [`Status \| undefined`](../../doc/models/status.md) | Optional | The finding's status as exposed in the UI. Status is a derived property combining information from the finding `state` and `triage_state`. The `triage_state` can be used to override the scan state if the finding is still detected |
| `syntacticId` | `string \| undefined` | Optional | ID calculated based on a finding's file path, rule identifier and matched code, and index. Prefer `match_based_id` |
| `triageComment` | `string \| undefined` | Optional | The detailed comment provided during triage |
| `triageReason` | [`TriageReason \| undefined`](../../doc/models/triage-reason.md) | Optional | Reason provided when this issue was triaged |
| `triageState` | [`TriageState \| undefined`](../../doc/models/triage-state.md) | Optional | The finding's triage state. Note: "reviewing" and "fixing" are only in private beta. Set by the user and used along with state to generate the final "status" viewable in the UI |
| `triagedAt` | `string \| undefined` | Optional | When the finding was triaged |
| `usage` | [`Usage \| undefined`](../../doc/models/usage.md) | Optional | Usage of the vulnerable package in the codebase. Applies to reachable findings |
| `vulnerabilityIdentifier` | `string \| undefined` | Optional | Identifier of the vulnerability in the vulnerability database |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence1,
  Reachability,
  ScaFinding,
  Severity1,
  State,
  Status,
  TriageReason,
  TriageState,
} from 'apimatic-semgrep-sdk';

const scaFinding: ScaFinding = {
  categories: [
    'security'
  ],
  confidence: Confidence1.Medium,
  createdAt: '2020-11-18 23:28:12.391807+00:00',
  epssScore: {
    percentile: 236.52,
    score: 242.58,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  externalTicket: {
    externalSlug: 'external_slug4',
    id: BigInt(228),
    linkedIssueIds: [
      BigInt(115),
      BigInt(116),
      BigInt(117)
    ],
    url: 'url8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  firstSeenScanId: BigInt(1234),
  id: BigInt(1234567),
  isMalicious: true,
  lineOfCodeUrl: 'https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1',
  matchBasedId: '0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1',
  reachability: Reachability.Reachable,
  reachableCondition: 'you use the package on a host running Linux or MacOS',
  ref: 'refs/pull/1234/merge',
  relevantSince: '2020-11-18 23:28:12.391807+00:00',
  ruleName: 'typescript.react.security.audit.react-no-refs.react-no-refs',
  severity: Severity1.Medium,
  state: State.Unresolved,
  stateUpdatedAt: '2020-11-19 23:28:12.391807+00:00',
  status: Status.Open,
  syntacticId: '440eeface888e78afceac3dc7d4cc2cf',
  triageComment: 'This finding is from the test repo',
  triageReason: TriageReason.AcceptableRisk,
  triageState: TriageState.Untriaged,
  triagedAt: '2020-11-19 23:28:12.391807+00:00',
  vulnerabilityIdentifier: 'CVE-2021-24112',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

