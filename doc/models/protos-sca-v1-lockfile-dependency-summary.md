
# Protos Sca V1 Lockfile Dependency Summary

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1LockfileDependencySummary`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lockfilePath` | `string \| undefined` | Optional | Path to lockfile (e.g. foo/bar/package-lock.json). |
| `numDependencies` | `bigint \| undefined` | Optional | Total number of dependencies in the lockfile. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1LockfileDependencySummary } from 'apimatic-semgrep-sdk';

const protosScaV1LockfileDependencySummary: ProtosScaV1LockfileDependencySummary = {
  lockfilePath: 'lockfilePath6',
  numDependencies: BigInt(152),
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

