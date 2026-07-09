
# List Lockfiles for Dependencies Request

*This model accepts additional fields of type unknown.*

## Structure

`ListLockfilesForDependenciesRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Use cursor in response to get next page of results. |
| `dependencyFilter` | [`ProtosScaV1DependencyFilter \| undefined`](../../doc/models/protos-sca-v1-dependency-filter.md) | Optional | Object to provide dependency details to filter by. |
| `deploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `pageSize` | `bigint \| undefined` | Optional | Number of repositories per page. Default: 5, min: 1, max: 100.<br><br>**Default**: `5`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `repositoryId` | `string` | Required | Repository ID to filter by. Use Projects endpoints to retrieve repository IDs. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Ecosystem,
  LicensePolicySettings,
  ListLockfilesForDependenciesRequest,
} from 'apimatic-semgrep-sdk';

const listLockfilesForDependenciesRequest: ListLockfilesForDependenciesRequest = {
  deploymentId: 'deploymentId2',
  repositoryId: 'repositoryId4',
  cursor: 'cursor6',
  dependencyFilter: {
    ecosystem: Ecosystem.Mix,
    license: [
      'license1',
      'license2'
    ],
    licensePolicySettings: LicensePolicySettings.LicensePolicySettingBlock,
    lockfilePath: 'lockfilePath6',
    name: 'name2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  pageSize: BigInt(100),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

