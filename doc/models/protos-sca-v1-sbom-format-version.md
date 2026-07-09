
# Protos Sca V1 Sbom Format Version

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1SbomFormatVersion`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cyclonedxVersion` | [`CyclonedxVersion \| undefined`](../../doc/models/cyclonedx-version.md) | Optional | CycloneDX schema version for the SBOM export. Supported: 1.4, 1.5, 1.6, 1.7. Defaults to 1.4 when unset.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_CYCLONE_DX_VERSION_V1_4 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_5 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_6 \|  \|<br>\| SBOM_CYCLONE_DX_VERSION_V1_7 \|  \| |
| `format` | [`Format \| undefined`](../../doc/models/format.md) | Optional | Format for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_FORMAT_CYCLONEDX \|  \|<br><br>**Default**: `Format.SbomFormatCyclonedx` |
| `version` | `string \| undefined` | Optional | Deprecated. Use `cyclonedx_version`. Free-text CycloneDX version, e.g. "1.7". |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  CyclonedxVersion,
  Format,
  ProtosScaV1SbomFormatVersion,
} from 'apimatic-semgrep-sdk';

const protosScaV1SbomFormatVersion: ProtosScaV1SbomFormatVersion = {
  cyclonedxVersion: CyclonedxVersion.SbomCycloneDxVersionV16,
  format: Format.SbomFormatCyclonedx,
  version: 'version6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

