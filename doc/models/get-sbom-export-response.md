
# Get Sbom Export Response

*This model accepts additional fields of type unknown.*

## Structure

`GetSbomExportResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `downloadUrl` | `string \| undefined` | Optional | URL to download the SBOM when status is COMPLETED. |
| `errorMessage` | `string \| undefined` | Optional | Error message when status is FAILED. |
| `status` | [`Status3`](../../doc/models/status-3.md) | Required | Status of the SBOM export job.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SBOM_EXPORT_STATUS_IN_PROGRESS \| The SBOM export job is in progress. \|<br>\| SBOM_EXPORT_STATUS_COMPLETED \| The SBOM export job has completed. \|<br>\| SBOM_EXPORT_STATUS_FAILED \| The SBOM export job has failed. \| |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { GetSbomExportResponse, Status3 } from 'apimatic-semgrep-sdk';

const getSbomExportResponse: GetSbomExportResponse = {
  status: Status3.SbomExportStatusCompleted,
  downloadUrl: 'downloadUrl6',
  errorMessage: 'errorMessage2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

