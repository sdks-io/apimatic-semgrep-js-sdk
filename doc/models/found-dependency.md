
# Found Dependency

Information about the vulnerable package that was found in the codebase

*This model accepts additional fields of type unknown.*

## Structure

`FoundDependency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ecosystem` | [`Ecosystem2 \| undefined`](../../doc/models/ecosystem-2.md) | Optional | Ecosystem of the package<br><br>**Default**: `Ecosystem2.NoPackageManager` |
| `lockfileLineUrl` | `string \| undefined` | Optional | URL to the specific line in the lockfile where the dependency is listed |
| `mPackage` | `string \| undefined` | Optional | Name of the package that contains the vulnerability |
| `transitivity` | [`Transitivity2 \| undefined`](../../doc/models/transitivity-2.md) | Optional | Indicates whether the dependency is direct or transitive |
| `version` | `string \| undefined` | Optional | Version of the package that was found to be vulnerable |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Ecosystem2,
  FoundDependency,
  Transitivity2,
} from 'apimatic-semgrep-sdk';

const foundDependency: FoundDependency = {
  ecosystem: Ecosystem2.Npm,
  lockfileLineUrl: 'https://github.com/yourorg/yourrepo/blob/main/package-lock.json#L25',
  mPackage: 'System.Drawing.Common',
  transitivity: Transitivity2.Direct,
  version: '5.0.0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

