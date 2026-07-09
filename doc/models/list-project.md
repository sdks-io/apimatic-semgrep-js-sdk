
# List Project

A project in your organization that uses Semgrep.

*This model accepts additional fields of type unknown.*

## Structure

`ListProject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | Time when this project was created. |
| `defaultBranch` | `string \| undefined` | Optional | The default branch in the SCM. |
| `id` | `bigint` | Required | Unique ID of this project. |
| `latestScanAt` | `string \| undefined` | Optional | Time of latest scan, if there is one. |
| `name` | `string` | Required | Name of the project. |
| `primaryBranch` | `string \| undefined` | Optional | The primary branch of the project, if known. |
| `tags` | `string[]` | Required | Tags associated to this project. |
| `url` | `string \| undefined` | Optional | URL of the project, if there is one. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ListProject } from 'apimatic-semgrep-sdk';

const listProject: ListProject = {
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
};
```

