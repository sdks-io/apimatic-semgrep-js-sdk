
# Protos Openapi V1 Get Scan Response Scan Meta

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1GetScanResponseScanMeta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mTrue` | `string \| undefined` | Optional | What triggered this scan, if applicable. |
| `branch` | `string \| undefined` | Optional | The branch that was scanned, if applicable. |
| `commit` | `string \| undefined` | Optional | The commit SHA associated with the scan, if applicable. |
| `config` | `string \| undefined` | Optional | The path of the configuration file used for this scan, if applicable. |
| `repoUrl` | `string \| undefined` | Optional | The URL of the scanned repository, if applicable. |
| `ciJobUrl` | `string \| undefined` | Optional | The URL of the CI job that ran the scan, if applicable. |
| `repository` | `string \| undefined` | Optional | The name and organization of the scanned repository, if applicable. |
| `commitTitle` | `string \| undefined` | Optional | The commit message associated with the scan, if applicable. |
| `pullRequestId` | `string \| undefined` | Optional | The ID of the pull request associated with the scan, if applicable. |
| `pullRequestTitle` | `string \| undefined` | Optional | The title of the pull request associated with the scan if applicable. |
| `commitAuthorName` | `string \| undefined` | Optional | The name of the author of the commit associated with the scan, if applicable. |
| `commitAuthorImageUrl` | `string \| undefined` | Optional | The avatar image url of the author of the commit associated with the scan, if applicable. |
| `commitAuthorEmail` | `string \| undefined` | Optional | The email of the author of the commit associated with the scan, if applicable. |
| `commitAuthorUsername` | `string \| undefined` | Optional | The username of the author of the commit associated with the scan, if applicable. |
| `pullRequestAuthorUsername` | `string \| undefined` | Optional | The username of the author of the pull request associated with the scan, if applicable. |
| `pullRequestAuthorImageUrl` | `string \| undefined` | Optional | The avatar image url of the author of the pull request associated with the scan, if applicable. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1GetScanResponseScanMeta } from 'apimatic-semgrep-sdk';

const protosOpenapiV1GetScanResponseScanMeta: ProtosOpenapiV1GetScanResponseScanMeta = {
  mTrue: 'pull_request',
  branch: 'refs/heads/main',
  commit: '94c5be1312a9da03b7c4bfcc1c50b4379c83412',
  config: 'r/python',
  repoUrl: 'https://github.com/semgrep/semgrep',
  ciJobUrl: 'https://github.com/semgrep/semgrep/actions/runs/12345',
  repository: 'semgrep/semgrep',
  commitTitle: '{\n  "fix(feature)": "Added XYZ component"\n}',
  pullRequestId: '12345',
  pullRequestTitle: '{\n  "fix(feature)": "Added XYZ component"\n}',
  commitAuthorName: 'Sven Greppe',
  commitAuthorImageUrl: 'https://github.com/link/to/avatar.png',
  commitAuthorEmail: 'sven.greppe@semgrep.com',
  commitAuthorUsername: 'SvenGreppe',
  pullRequestAuthorUsername: 'SvenGreppe',
  pullRequestAuthorImageUrl: 'https://github.com/link/to/avatar.png',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

