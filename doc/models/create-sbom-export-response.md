
# Create Sbom Export Response

*This model accepts additional fields of type unknown.*

## Structure

`CreateSbomExportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `taskToken` | `string` | Required | Task token for the SBOM export job. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CreateSbomExportResponse } from 'apimatic-semgrep-sdk';

const createSbomExportResponse: CreateSbomExportResponse = {
  taskToken: 'taskToken6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

