
# Get Project Response

Successfully retrieved details for the project.

*This model accepts additional fields of type unknown.*

## Structure

`GetProjectResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `project` | [`Project`](../../doc/models/project.md) | Required | A project in your organization that uses Semgrep. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { GetProjectResponse } from 'apimatic-semgrep-sdk';

const getProjectResponse: GetProjectResponse = {
  project: {
    id: BigInt(1234567),
    name: 'returntocorp/semgrep',
    tags: [
      'tag'
    ],
    createdAt: '2020-11-18 23:28:12.391807+00:00',
    defaultBranch: 'refs/heads/main',
    latestScanAt: '2023-01-13 20:51:51.449081+00:00',
    managedScanConfig: {
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
    },
    primaryBranch: 'refs/heads/custom-main',
    url: 'https://github.com/returntocorp/semgrep',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

