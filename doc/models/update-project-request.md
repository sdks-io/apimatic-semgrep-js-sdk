
# Update Project Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdateProjectRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. |
| `managedScanConfig` | [`ManagedScanConfig \| undefined`](../../doc/models/managed-scan-config.md) | Optional | [Beta] Configuration of Semgrep Managed Scans for the project, if relevant. |
| `primaryBranch` | `string \| undefined` | Optional | The full name of the branch you would like to set as primary. Use "None" if default_branch is known and you wish to set primary to always be the default branch. |
| `projectName` | `string` | Required | Name of the project, typically the repository formatted as a path. |
| `tags` | `string[] \| undefined` | Optional | Tags associated to this project. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { UpdateProjectRequest } from 'apimatic-semgrep-sdk';

const updateProjectRequest: UpdateProjectRequest = {
  deploymentSlug: 'your-deployment',
  projectName: 'organization/project',
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
  primaryBranch: 'refs/heads/develop',
  tags: [
    'tag'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

