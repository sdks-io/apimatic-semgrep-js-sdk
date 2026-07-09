
# Protos Sca V1 Package Filter

Individual package filter with optional version bounds.

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1PackageFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `exactNameMatch` | `boolean \| undefined` | Optional | When true, name must match exactly. When false (default), name is fuzzy-matched (contains). |
| `exactVersion` | `string \| undefined` | Optional | Exact version match (e.g. "1.0.0").<br>Takes precedence over version bounds if set. |
| `name` | `string \| undefined` | Optional | Exact package name (e.g. lodash). |
| `versionLowerBound` | `string \| undefined` | Optional | Lower bound version constraint (e.g. ">=1.0.0").<br>Ignored if exact_version is set. |
| `versionUpperBound` | `string \| undefined` | Optional | Upper bound version constraint (e.g. "<2.0.0").<br>Ignored if exact_version is set. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1PackageFilter } from 'apimatic-semgrep-sdk';

const protosScaV1PackageFilter: ProtosScaV1PackageFilter = {
  exactNameMatch: false,
  exactVersion: 'exactVersion4',
  name: 'name6',
  versionLowerBound: 'versionLowerBound8',
  versionUpperBound: 'versionUpperBound8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

