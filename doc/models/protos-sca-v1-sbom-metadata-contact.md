
# Protos Sca V1 Sbom Metadata Contact

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScaV1SbomMetadataContact`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `email` | `string \| undefined` | Optional | - |
| `name` | `string \| undefined` | Optional | - |
| `phone` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScaV1SbomMetadataContact } from 'apimatic-semgrep-sdk';

const protosScaV1SbomMetadataContact: ProtosScaV1SbomMetadataContact = {
  email: 'email0',
  name: 'name6',
  phone: 'phone6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

