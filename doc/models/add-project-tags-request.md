
# Add Project Tags Request

*This model accepts additional fields of type unknown.*

## Structure

`AddProjectTagsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Required | Slug of the deployment name. Can be found at `/deployments`, or in your Settings in the web UI. |
| `projectName` | `string` | Required | Name of the project, typically the repository formatted as a path. |
| `tags` | `string[] \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { AddProjectTagsRequest } from 'apimatic-semgrep-sdk';

const addProjectTagsRequest: AddProjectTagsRequest = {
  deploymentSlug: 'your-deployment',
  projectName: 'organization/project',
  tags: [
    'tag'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

