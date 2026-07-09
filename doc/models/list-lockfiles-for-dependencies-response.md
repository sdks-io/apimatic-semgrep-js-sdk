
# List Lockfiles for Dependencies Response

*This model accepts additional fields of type unknown.*

## Structure

`ListLockfilesForDependenciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Pass to next request to get next page of results. |
| `hasMore` | `boolean` | Required | True if there are more lockfiles to get. |
| `lockfileSummaries` | [`ProtosScaV1LockfileDependencySummary[]`](../../doc/models/protos-sca-v1-lockfile-dependency-summary.md) | Required | List of lockfiles. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ListLockfilesForDependenciesResponse } from 'apimatic-semgrep-sdk';

const listLockfilesForDependenciesResponse: ListLockfilesForDependenciesResponse = {
  hasMore: false,
  lockfileSummaries: [
    {
      lockfilePath: 'lockfilePath8',
      numDependencies: BigInt(0),
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  cursor: 'cursor0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

