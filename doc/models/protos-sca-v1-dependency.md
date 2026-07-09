
# Protos Sca V1 Dependency

A specific dependency.

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1Dependency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | String identifier of dependency |
| `versionSpecifier` | `string \| undefined` | Optional | Version specifier of dependency. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1Dependency } from 'apimatic-semgrep-sdk';

const protosScaV1Dependency: ProtosScaV1Dependency = {
  name: 'name2',
  versionSpecifier: 'versionSpecifier0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

