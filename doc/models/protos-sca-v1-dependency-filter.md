
# Protos Sca V1 Dependency Filter

Object to provide dependency details to filter by.

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1DependencyFilter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ecosystem` | [`Ecosystem \| undefined`](../../doc/models/ecosystem.md) | Optional | Filter by ecosystem (e.g. npm, pypi, etc).<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| no_package_manager \|  \|<br>\| npm \|  \|<br>\| pypi \|  \|<br>\| gomod \|  \|<br>\| cargo \|  \|<br>\| maven \|  \|<br>\| gem \|  \|<br>\| composer \|  \|<br>\| nuget \|  \|<br>\| pub \|  \|<br>\| swiftpm \|  \|<br>\| hex \|  \|<br>\| cocoapods \|  \|<br>\| mix \|  \|<br>\| opam \|  \| |
| `license` | `string[] \| undefined` | Optional | Filter by license (e.g. MIT). |
| `licensePolicySettings` | [`LicensePolicySettings \| undefined`](../../doc/models/license-policy-settings.md) | Optional | Filter by license policy setting outcome.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| LICENSE_POLICY_SETTING_ALLOW \|  \|<br>\| LICENSE_POLICY_SETTING_COMMENT \|  \|<br>\| LICENSE_POLICY_SETTING_BLOCK \|  \| |
| `lockfilePath` | `string \| undefined` | Optional | Filter by path to the lockfile (e.g. `foo/bar/package-lock.json`). |
| `name` | `string \| undefined` | Optional | Deprecated - use package_filters instead. Filter by dependency name (e.g. lodash). |
| `packageFilters` | [`ProtosScaV1PackageFilter[] \| undefined`](../../doc/models/protos-sca-v1-package-filter.md) | Optional | Multiple package filters with exact name matching and version bounds. |
| `repositoryId` | `bigint[] \| undefined` | Optional | Repository IDs (numeric) to filter by. Omit if the endpoint has Repository ID as a path parameter.<br>Use Projects endpoints to retrieve Repository IDs. |
| `transitivity` | [`Transitivity \| undefined`](../../doc/models/transitivity.md) | Optional | Filter by transitivity.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| UNKNOWN_TRANSITIVITY \|  \|<br>\| TRANSITIVE \|  \|<br>\| DIRECT \|  \| |
| `version` | `string \| undefined` | Optional | Deprecated - use package_filters instead. Filter by dependency version (e.g. 1.0.1). |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Ecosystem,
  LicensePolicySettings,
  ProtosScaV1DependencyFilter,
} from 'apimatic-semgrep-sdk';

const protosScaV1DependencyFilter: ProtosScaV1DependencyFilter = {
  ecosystem: Ecosystem.Opam,
  license: [
    'license5'
  ],
  licensePolicySettings: LicensePolicySettings.LicensePolicySettingBlock,
  lockfilePath: 'lockfilePath0',
  name: 'name8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

