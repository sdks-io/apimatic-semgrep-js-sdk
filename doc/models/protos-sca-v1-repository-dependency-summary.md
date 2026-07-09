
# Protos Sca V1 Repository Dependency Summary

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1RepositoryDependencySummary`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `hasDependencyPathScan` | `boolean \| undefined` | Optional | True if the repository has been scanned with the `hasPathToTransitivityInScans` feature flag<br>which means it will have dependency graph data in DGraph available to query |
| `id` | `bigint \| undefined` | Optional | ID of repository. |
| `name` | `string \| undefined` | Optional | Name of repository. |
| `numDependencies` | `bigint \| undefined` | Optional | Total number of dependencies in the repository. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1RepositoryDependencySummary } from 'apimatic-semgrep-sdk';

const protosScaV1RepositoryDependencySummary: ProtosScaV1RepositoryDependencySummary = {
  hasDependencyPathScan: false,
  id: BigInt(78),
  name: 'name4',
  numDependencies: BigInt(164),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

