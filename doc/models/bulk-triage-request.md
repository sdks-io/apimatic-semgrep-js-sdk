
# Bulk Triage Request

*This model accepts additional fields of type unknown.*

## Structure

`BulkTriageRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autotriageVerdict` | [`AutotriageVerdict \| undefined`](../../doc/models/autotriage-verdict.md) | Optional | The autotriage verdict to filter by |
| `categories` | `string[] \| undefined` | Optional | List of categories to filter by |
| `componentTags` | `string[] \| undefined` | Optional | List of component tags to filter by |
| `confidence` | [`Confidence3 \| undefined`](../../doc/models/confidence-3.md) | Optional | List of confidence levels to filter by |
| `dependencies` | `string[] \| undefined` | Optional | Filter by dependency name. Only applies for sca findings. |
| `epssProbability` | [`EpssProbability \| undefined`](../../doc/models/epss-probability.md) | Optional | Filter by EPSS probability (likelihood of exploit). Only applies for sca findings. |
| `exposures` | [`Exposures \| undefined`](../../doc/models/exposures.md) | Optional | Filter by exposure (reachability type). Only applies for sca findings. Reachability is the ability of an attacker to access a vulnerability in a system. |
| `includeHistorical` | `boolean \| undefined` | Optional | Whether to include historical findings. Only applies for secrets findings. Defaults to true. |
| `issueIds` | `bigint[] \| undefined` | Optional | An array of issue IDs to act on. If this is not provided, an issue filter should be provided. |
| `issueType` | [`IssueType`](../../doc/models/issue-type.md) | Required | Type of findings to bulk triage. |
| `limit` | `bigint \| undefined` | Optional | Max number of issues to triage. Must be an integer between 1 and 3000. Defaults to 3000. When selecting findings to triage, Semgrep will also triage findings with the same fingerprint on other branches. As a result, the list of triaged issue_ids returned in the response may be higher than the specified limit.<br><br>**Default**: `3000` |
| `newNote` | `string \| undefined` | Optional | The note to attach to the bulk triaged findings. Maximum 3000 characters. |
| `newTriageReason` | [`NewTriageReason \| undefined`](../../doc/models/new-triage-reason.md) | Optional | The reason for triaging to a given triage state. |
| `newTriageState` | [`NewTriageState \| undefined`](../../doc/models/new-triage-state.md) | Optional | The triage state you would like to bulk triage your findings to. |
| `policies` | `string[] \| undefined` | Optional | List of policy modes to filter by |
| `policyMode` | [`PolicyMode1 \| undefined`](../../doc/models/policy-mode-1.md) | Optional | List of policy modes to filter by |
| `proOnly` | `boolean \| undefined` | Optional | Filter by whether a finding is only available with Semgrep Pro features. |
| `projectTags` | `string[] \| undefined` | Optional | List of project tags to filter by |
| `ref` | `string \| undefined` | Optional | Branch reference to filter by |
| `repos` | `string[] \| undefined` | Optional | List of repository names to filter by |
| `repositoryVisibility` | [`RepositoryVisibility \| undefined`](../../doc/models/repository-visibility.md) | Optional | Filter by repository visibility. Only applies for secrets findings. |
| `rules` | `string[] \| undefined` | Optional | List of rule names to filter by |
| `ruleset` | `string[] \| undefined` | Optional | List of Semgrep Registry rulesets to filter by |
| `secretTypes` | `string[] \| undefined` | Optional | Filter by type of secret (typically provider-related). Only applies for secrets findings. |
| `severities` | [`Severities \| undefined`](../../doc/models/severities.md) | Optional | List of severities to filter by |
| `since` | `string \| undefined` | Optional | Epoch timestamp in seconds. Filters using the relevant_since field: the timestamp when this finding was detected by Semgrep (the first time, or when reintroduced). |
| `status` | [`Status1 \| undefined`](../../doc/models/status-1.md) | Optional | The status to filter by |
| `transitivities` | [`Transitivities \| undefined`](../../doc/models/transitivities.md) | Optional | Filter by transitivity of a dependency. Only applies for sca findings. |
| `triageReasons` | [`TriageReasons \| undefined`](../../doc/models/triage-reasons.md) | Optional | List of triage reasons to filter by |
| `validationState` | [`ValidationState \| undefined`](../../doc/models/validation-state.md) | Optional | Filter by whether a secret could be validated. Only applies for secrets findings. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  AutotriageVerdict,
  BulkTriageRequest,
  Confidence3,
  IssueType,
  NewTriageReason,
  NewTriageState,
  Status1,
} from 'apimatic-semgrep-sdk';

const bulkTriageRequest: BulkTriageRequest = {
  issueType: IssueType.Sca,
  autotriageVerdict: AutotriageVerdict.TruePositive,
  categories: [
    'security',
    'performance'
  ],
  componentTags: [
    'user authentication',
    'user data'
  ],
  confidence: Confidence3.High,
  dependencies: [
    'lodash',
    'express'
  ],
  includeHistorical: true,
  issueIds: [
    BigInt(123),
    BigInt(456)
  ],
  limit: BigInt(100),
  newNote: 'some note here',
  newTriageReason: NewTriageReason.AcceptableRisk,
  newTriageState: NewTriageState.Reopened,
  policies: [
    'rule-board-block',
    'rule-board-pr-comments',
    'rule-board-audit'
  ],
  proOnly: true,
  projectTags: [
    'my_project_tag_1',
    'my_project_tag_2'
  ],
  ref: 'refs/pull/1234/merge',
  repos: [
    'myorg/repo1',
    'myorg/repo2'
  ],
  rules: [
    'typescript.react.security.audit.react-no-refs.react-no-refs',
    'ajinabraham.njsscan.hardcoded_secrets.node_username'
  ],
  ruleset: [
    'owasp-top-ten',
    'default'
  ],
  secretTypes: [
    'Github',
    'Heroku',
    'AWS'
  ],
  since: '1717334400',
  status: Status1.Open,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

