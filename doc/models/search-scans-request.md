
# Search Scans Request

*This model accepts additional fields of type unknown.*

## Structure

`SearchScansRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `branch` | `string \| undefined` | Optional | Only get scans from the specified branch |
| `cursor` | `string \| undefined` | Optional | Cursor to paginate through the results |
| `deploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `isFullScan` | `number \| undefined` | Optional | Only get scans that are full scans (if false, only get diff scans) |
| `limit` | `number \| undefined` | Optional | Page size to paginate through the results (default is 100, max is 500) |
| `products` | [`Products \| undefined`](../../doc/models/products.md) | Optional | Only get scans that have these enabled products<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| PRODUCT_SAST \|  \|<br>\| PRODUCT_SCA \|  \|<br>\| PRODUCT_SECRETS \|  \|<br>\| PRODUCT_AI_SAST \|  \| |
| `repositoryId` | `number \| undefined` | Optional | Only get scans for this repo |
| `since` | `string \| undefined` | Optional | Only get scans created after this time. Provide time in ISO 8601 format. |
| `statuses` | [`Statuses \| undefined`](../../doc/models/statuses.md) | Optional | Only get scans that have one of these statuses<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SCAN_STATUS_RUNNING \| The scan is currently running \|<br>\| SCAN_STATUS_COMPLETED \| The scan has completed successfully (0 or 1 exit code) \|<br>\| SCAN_STATUS_PENDING \| The scan is queued and waiting to start \|<br>\| SCAN_STATUS_CANCELLED \| The scan was cancelled before completion \|<br>\| SCAN_STATUS_ERROR \| The scan has exited with a failure (exit code not 0 or 1) \|<br>\| SCAN_STATUS_NEVER_FINISHED \| The scan did not report an error or success after over an hour \| |
| `totalTime` | [`FloatRange \| undefined`](../../doc/models/float-range.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Products, SearchScansRequest } from 'apimatic-semgrep-sdk';

const searchScansRequest: SearchScansRequest = {
  deploymentId: '123',
  branch: 'branch6',
  cursor: 'cursor6',
  isFullScan: 26,
  limit: 236,
  products: Products.ProductSast,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

