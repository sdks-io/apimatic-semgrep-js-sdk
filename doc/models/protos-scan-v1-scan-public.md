
# Protos Scan V1 Scan Public

*This model accepts additional fields of type unknown.*

## Structure

`ProtosScanV1ScanPublic`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `string \| undefined` | Optional | The scanned branch |
| `commit` | `string \| undefined` | Optional | The commit hash that was scanned |
| `completedAt` | `string \| undefined` | Optional | The timestamp when this scan completed (if it has completed). |
| `deploymentId` | `string \| undefined` | Optional | Unique identifier for the deployment of the scan. |
| `enabledProducts` | `string[] \| undefined` | Optional | The products used when running the scan. |
| `exitCode` | `string \| undefined` | Optional | The exit_code of the scan (see https://semgrep.dev/docs/cli-reference#exit-codes) |
| `findingsCounts` | [`ProtosScanV1ScanFindingsCounts \| undefined`](../../doc/models/protos-scan-v1-scan-findings-counts.md) | Optional | - |
| `id` | `string \| undefined` | Optional | ID of the scan. |
| `isFullScan` | `boolean \| undefined` | Optional | Whether the scan was a full scan (true) or a diff scan (false) |
| `repositoryId` | `string \| undefined` | Optional | Unique identifier for the repository of the scan. |
| `startedAt` | `string \| undefined` | Optional | The timestamp when this scan started. |
| `status` | [`Status7 \| undefined`](../../doc/models/status-7.md) | Optional | The current status of the scan<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCAN_STATUS_RUNNING \| The scan is currently running \|<br>\| SCAN_STATUS_COMPLETED \| The scan has completed successfully (0 or 1 exit code) \|<br>\| SCAN_STATUS_PENDING \| The scan is queued and waiting to start \|<br>\| SCAN_STATUS_CANCELLED \| The scan was cancelled before completion \|<br>\| SCAN_STATUS_ERROR \| The scan has exited with a failure (exit code not 0 or 1) \|<br>\| SCAN_STATUS_NEVER_FINISHED \| The scan did not report an error or success after over an hour \| |
| `totalTime` | `number \| undefined` | Optional | Duration of scan, in seconds |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosScanV1ScanPublic, Status7 } from 'apimatic-semgrep-sdk';

const protosScanV1ScanPublic: ProtosScanV1ScanPublic = {
  branch: 'main',
  commit: '6d3de02545f820febf2af9820568fa5f697d4087',
  completedAt: '2020-11-18 23:30:10.216670+00:00',
  deploymentId: 'deployment_id0',
  enabledProducts: [
    'secrets'
  ],
  exitCode: '0',
  isFullScan: true,
  startedAt: '2020-11-18 23:28:12.391807+00:00',
  status: Status7.ScanStatusRunning,
  totalTime: 17.32,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

