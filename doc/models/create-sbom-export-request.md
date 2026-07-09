
# Create Sbom Export Request

*This model accepts additional fields of type unknown.*

## Structure

`CreateSbomExportRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `formatVersion` | [`ProtosScaV1SbomFormatVersion \| undefined`](../../doc/models/protos-sca-v1-sbom-format-version.md) | Optional | - |
| `metadataComponentType` | [`MetadataComponentType \| undefined`](../../doc/models/metadata-component-type.md) | Optional | Metadata component type for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_APPLICATION \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FRAMEWORK \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_LIBRARY \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_CONTAINER \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_PLATFORM \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_OPERATING_SYSTEM \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DEVICE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DEVICE_DRIVER \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FIRMWARE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_FILE \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_MACHINE_LEARNING_MODEL \|  \|<br>\| SBOM_METADATA_COMPONENT_TYPE_CYCLONE_DX_V15_DATA \|  \|<br><br>**Default**: `MetadataComponentType.SbomMetadataComponentTypeCycloneDxV15Application` |
| `metadataSupplier` | [`ProtosScaV1SbomMetadataSupplier \| undefined`](../../doc/models/protos-sca-v1-sbom-metadata-supplier.md) | Optional | - |
| `ref` | `string \| undefined` | Optional | Branch to export SBOM for (Ex. ref=`refs/pull/1234/merge`). |
| `repositoryId` | `string \| undefined` | Optional | Repository ID to export SBOM for. |
| `sbomOutputFormat` | [`SbomOutputFormat \| undefined`](../../doc/models/sbom-output-format.md) | Optional | SBOM output format for the SBOM export.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_OUTPUT_FORMAT_JSON \|  \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  CreateSbomExportRequest,
  CyclonedxVersion,
  Format,
  MetadataComponentType,
  SbomOutputFormat,
} from 'apimatic-semgrep-sdk';

const createSbomExportRequest: CreateSbomExportRequest = {
  deploymentId: '123',
  formatVersion: {
    cyclonedxVersion: CyclonedxVersion.SbomCycloneDxVersionV16,
    format: Format.SbomFormatCyclonedx,
    version: 'version8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  metadataComponentType: MetadataComponentType.SbomMetadataComponentTypeCycloneDxV15Application,
  metadataSupplier: {
    contact: {
      email: 'email4',
      name: 'name2',
      phone: 'phone2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    name: 'name4',
    url: 'url8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  ref: 'refs/pull/1234/merge',
  repositoryId: '123',
  sbomOutputFormat: SbomOutputFormat.SbomOutputFormatJson,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

