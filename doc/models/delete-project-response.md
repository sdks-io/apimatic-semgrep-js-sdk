
# Delete Project Response

Successfully deleted the project.

*This model accepts additional fields of type unknown.*

## Structure

`DeleteProjectResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `projectName` | `string` | Required | The name of the deleted project. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { DeleteProjectResponse } from 'apimatic-semgrep-sdk';

const deleteProjectResponse: DeleteProjectResponse = {
  projectName: 'organization/project',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

