
# Protos Sca V1 Sbom Metadata Supplier

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1SbomMetadataSupplier`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `contact` | [`ProtosScaV1SbomMetadataContact \| undefined`](../../doc/models/protos-sca-v1-sbom-metadata-contact.md) | Optional | - |
| `name` | `string \| undefined` | Optional | - |
| `url` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1SbomMetadataSupplier } from 'apimatic-semgrep-sdk';

const protosScaV1SbomMetadataSupplier: ProtosScaV1SbomMetadataSupplier = {
  contact: {
    email: 'email4',
    name: 'name2',
    phone: 'phone2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  name: 'name2',
  url: 'url6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

