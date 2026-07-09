
# Status 3

Status of the SBOM export job.

| value | description |
|-------|---------------|
| SBOM_EXPORT_STATUS_IN_PROGRESS | The SBOM export job is in progress. |
| SBOM_EXPORT_STATUS_COMPLETED | The SBOM export job has completed. |
| SBOM_EXPORT_STATUS_FAILED | The SBOM export job has failed. |

## Enumeration

`Status3`

## Fields

| Name |
|  --- |
| `SbomExportStatusInProgress` |
| `SbomExportStatusCompleted` |
| `SbomExportStatusFailed` |

## Example

```ts
import { Status3 } from 'apimatic-semgrep-sdk';

const status3 = Status3.SbomExportStatusCompleted;
```

