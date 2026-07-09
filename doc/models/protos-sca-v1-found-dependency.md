
# Protos Sca V1 Found Dependency

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1FoundDependency`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `definedAt` | [`ProtosScaV1CodeLocation \| undefined`](../../doc/models/protos-sca-v1-code-location.md) | Optional | Path and line number dependency is declared in. |
| `ecosystem` | [`Ecosystem1 \| undefined`](../../doc/models/ecosystem-1.md) | Optional | The ecosystem the dependency is in (e.g. pypi, npm, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| no_package_manager \|  \|<br>\| npm \|  \|<br>\| pypi \|  \|<br>\| gomod \|  \|<br>\| cargo \|  \|<br>\| maven \|  \|<br>\| gem \|  \|<br>\| composer \|  \|<br>\| nuget \|  \|<br>\| pub \|  \|<br>\| swiftpm \|  \|<br>\| hex \|  \|<br>\| cocoapods \|  \|<br>\| mix \|  \|<br>\| opam \|  \| |
| `licenses` | `string[] \| undefined` | Optional | Licenses the dependency is using. |
| `manifestDefinition` | [`ProtosScaV1CodeLocation \| undefined`](../../doc/models/protos-sca-v1-code-location.md) | Optional | Path to the manifest file that defines the subproject containing this dependency |
| `mPackage` | [`ProtosScaV1Dependency \| undefined`](../../doc/models/protos-sca-v1-dependency.md) | Optional | What the dependency is. |
| `repositoryId` | `string \| undefined` | Optional | ID of repository dependency is found in. |
| `resolvedUrl` | `string \| undefined` | Optional | The resolved URL of the dependency. Could point to a compressed source code directory (e.g. tarball), source code repository, or a package manager cache directory. May be empty if the package manager doesn't supply a URL. |
| `transitivity` | [`Transitivity1 \| undefined`](../../doc/models/transitivity-1.md) | Optional | Whether dependency is direct or transitive.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| UNKNOWN_TRANSITIVITY \|  \|<br>\| TRANSITIVE \|  \|<br>\| DIRECT \|  \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Ecosystem1, ProtosScaV1FoundDependency } from 'apimatic-semgrep-sdk';

const protosScaV1FoundDependency: ProtosScaV1FoundDependency = {
  definedAt: {
    committedAt: '2016-03-13T12:52:32.123Z',
    endCol: 'endCol8',
    endLine: 'endLine2',
    path: 'path2',
    startCol: 'startCol2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  ecosystem: Ecosystem1.Gem,
  licenses: [
    'licenses5',
    'licenses6',
    'licenses7'
  ],
  manifestDefinition: {
    committedAt: '2016-03-13T12:52:32.123Z',
    endCol: 'endCol0',
    endLine: 'endLine4',
    path: 'path4',
    startCol: 'startCol4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  mPackage: {
    name: 'name8',
    versionSpecifier: 'versionSpecifier6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

