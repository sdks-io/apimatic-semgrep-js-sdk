
# List Repositories for Dependencies Response

*This model accepts additional fields of type unknown.*

## Structure

`ListRepositoriesForDependenciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `bigint \| undefined` | Optional | Pass to next request to get next page of results. |
| `hasMore` | `boolean` | Required | True if there are more repositories to get. |
| `repositorySummaries` | [`ProtosScaV1RepositoryDependencySummary[]`](../../doc/models/protos-sca-v1-repository-dependency-summary.md) | Required | List of repositories. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ListRepositoriesForDependenciesResponse,
} from 'apimatic-semgrep-sdk';

const listRepositoriesForDependenciesResponse: ListRepositoriesForDependenciesResponse = {
  hasMore: false,
  repositorySummaries: [
    {
      hasDependencyPathScan: false,
      id: BigInt(140),
      name: 'name0',
      numDependencies: BigInt(226),
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  cursor: BigInt(48),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

