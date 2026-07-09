
# List Projects Response

Return the list of projects in an organization.

*This model accepts additional fields of type unknown.*

## Structure

`ListProjectsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projects` | [`ListProject[]`](../../doc/models/list-project.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ListProjectsResponse } from 'apimatic-semgrep-sdk';

const listProjectsResponse: ListProjectsResponse = {
  projects: [
    {
      id: BigInt(1234567),
      name: 'returntocorp/semgrep',
      tags: [
        'tag'
      ],
      createdAt: '2020-11-18 23:28:12.391807+00:00',
      defaultBranch: 'refs/heads/main',
      latestScanAt: '2023-01-13 20:51:51.449081+00:00',
      primaryBranch: 'refs/heads/custom-main',
      url: 'https://github.com/returntocorp/semgrep',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

