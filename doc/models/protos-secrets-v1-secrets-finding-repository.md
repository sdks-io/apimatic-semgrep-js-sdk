
# Protos Secrets V1 Secrets Finding Repository

Repository where the finding was detected.

*This model accepts additional fields of type unknown.*

## Structure

`ProtosSecretsV1SecretsFindingRepository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | Repository name |
| `scmType` | [`ScmType \| undefined`](../../doc/models/scm-type.md) | Optional | Provider for the finding (e.g. GitHub, GitLab, GHE, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCM_TYPE_GITHUB \| GitHub Cloud \|<br>\| SCM_TYPE_GITHUB_ENTERPRISE \| GitHub Enterprise \|<br>\| SCM_TYPE_GITLAB \| GitLab Cloud \|<br>\| SCM_TYPE_GITLAB_SELFMANAGED \| GitLab Self-Managed \|<br>\| SCM_TYPE_BITBUCKET \| Bitbucket Cloud \|<br>\| SCM_TYPE_BITBUCKET_DATACENTER \| Bitbucket Data Center \|<br>\| SCM_TYPE_AZURE_DEVOPS \| Azure DevOps \|<br>\| SCM_TYPE_UNKNOWN \|  \|<br>\| SCM_TYPE_HARNESS \| Harness \| |
| `url` | `string \| undefined` | Optional | URL to the repository where the finding was detected. |
| `visibility` | [`Visibility \| undefined`](../../doc/models/visibility.md) | Optional | Repository visbility (e.g. public, private, unknown).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| REPOSITORY_VISIBILITY_PUBLIC \|  \|<br>\| REPOSITORY_VISIBILITY_PRIVATE \|  \|<br>\| REPOSITORY_VISIBILITY_UNKNOWN \|  \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ProtosSecretsV1SecretsFindingRepository,
  ScmType,
  Visibility,
} from 'apimatic-semgrep-sdk';

const protosSecretsV1SecretsFindingRepository: ProtosSecretsV1SecretsFindingRepository = {
  name: 'name4',
  scmType: ScmType.ScmTypeBitbucketDatacenter,
  url: 'url8',
  visibility: Visibility.RepositoryVisibilityPrivate,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

