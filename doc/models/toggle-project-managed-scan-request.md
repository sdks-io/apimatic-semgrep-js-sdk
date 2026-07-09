
# Toggle Project Managed Scan Request

*This model accepts additional fields of type unknown.*

## Structure

`ToggleProjectManagedScanRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. |
| `diffScan` | [`ProtosOpenapiV1DiffScan \| undefined`](../../doc/models/protos-openapi-v1-diff-scan.md) | Optional | - |
| `fullScan` | [`ProtosOpenapiV1FullScan \| undefined`](../../doc/models/protos-openapi-v1-full-scan.md) | Optional | - |
| `projectName` | `string` | Required | Name of the project, typically the repository formatted as a path. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ToggleProjectManagedScanRequest } from 'apimatic-semgrep-sdk';

const toggleProjectManagedScanRequest: ToggleProjectManagedScanRequest = {
  deploymentSlug: 'your-deployment',
  projectName: 'organization/project',
  diffScan: {
    enabled: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  fullScan: {
    enabled: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

