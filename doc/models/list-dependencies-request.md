
# List Dependencies Request

*This model accepts additional fields of type unknown.*

## Structure

`ListDependenciesRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Cursor to paginate through the dependencies. Provide a cursor value from the response to retrieve the next page. |
| `dependencyFilter` | [`ProtosScaV1DependencyFilter \| undefined`](../../doc/models/protos-sca-v1-dependency-filter.md) | Optional | Object to provide dependency details to filter by. |
| `deploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `pageSize` | `bigint \| undefined` | Optional | Number of dependencies per page. Default: 1000, min: 1, max: 10000.<br><br>**Constraints**: `>= 1`, `<= 10000` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Ecosystem,
  LicensePolicySettings,
  ListDependenciesRequest,
} from 'apimatic-semgrep-sdk';

const listDependenciesRequest: ListDependenciesRequest = {
  deploymentId: '123',
  cursor: 'cursor2',
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
  pageSize: BigInt(1000),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

