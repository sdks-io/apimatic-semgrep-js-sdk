
# Create Ticket Request

Create ticket request

*This model accepts additional fields of type unknown.*

## Structure

`CreateTicketRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autotriageVerdict` | [`AutotriageVerdict \| undefined`](../../doc/models/autotriage-verdict.md) | Optional | The autotriage verdict to filter by |
| `categories` | `string[] \| undefined` | Optional | List of categories to filter by |
| `componentTags` | `string[] \| undefined` | Optional | List of component tags to filter by |
| `confidence` | [`Confidence3 \| undefined`](../../doc/models/confidence-3.md) | Optional | List of confidence levels to filter by |
| `dependencies` | `string[] \| undefined` | Optional | Filter by dependency name. Only applies for sca findings. |
| `deploymentSlug` | `string` | Required | Deployment slug. Can be found at `/deployments`, or in your Settings in the web UI. |
| `epssProbability` | [`EpssProbability \| undefined`](../../doc/models/epss-probability.md) | Optional | Filter by EPSS probability (likelihood of exploit). Only applies for sca findings. |
| `exposures` | [`Exposures \| undefined`](../../doc/models/exposures.md) | Optional | Filter by exposure (reachability type). Only applies for sca findings. Reachability is the ability of an attacker to access a vulnerability in a system. |
| `groupIssues` | `boolean \| undefined` | Optional | Whether or not to group findings from the same rule and repository into a single ticket. Defaults to true.<br><br>**Default**: `true` |
| `includeHistorical` | `boolean \| undefined` | Optional | Whether to include historical findings. Only applies for secrets findings. Defaults to true. |
| `issueIds` | `string[] \| undefined` | Optional | An array of issue IDs to act on. If this is not provided, an issue filter should be provided. |
| `issueType` | [`IssueType1`](../../doc/models/issue-type-1.md) | Required | Type of findings to create tickets for. |
| `jiraProjectId` | `string \| undefined` | Optional | Optional numeric Jira project ID to associate with the created tickets. If not specified, defaults to the project configured in your integration settings. You can fetch this ID using the Jira API. |
| `limit` | `bigint \| undefined` | Optional | Max number of tickets to create. Must be an integer between 1 and 20. Defaults to 20<br><br>**Default**: `20` |
| `policies` | `string[] \| undefined` | Optional | List of policy modes to filter by |
| `policyMode` | [`PolicyMode1 \| undefined`](../../doc/models/policy-mode-1.md) | Optional | List of policy modes to filter by |
| `proOnly` | `boolean \| undefined` | Optional | Filter by whether a finding is only available with Semgrep Pro features. Only applies for sast findings. |
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
  Confidence3,
  CreateTicketRequest,
  IssueType1,
  Status1,
} from 'apimatic-semgrep-sdk';

const createTicketRequest: CreateTicketRequest = {
  deploymentSlug: 'deploymentSlug6',
  issueType: IssueType1.Sca,
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
  groupIssues: true,
  includeHistorical: true,
  issueIds: [
    '123',
    '456'
  ],
  jiraProjectId: '12345',
  limit: BigInt(20),
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

