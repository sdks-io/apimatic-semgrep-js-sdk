
# Click to Fix Pr

A pull request created by Semgrep's Click to Fix feature

*This model accepts additional fields of type unknown.*

## Structure

`ClickToFixPr`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | When this PR was created |
| `url` | `string \| undefined` | Optional | URL of the pull request |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ClickToFixPr } from 'apimatic-semgrep-sdk';

const clickToFixPr: ClickToFixPr = {
  createdAt: '2024-01-15 10:30:00+00:00',
  url: 'https://github.com/myorg/myrepo/pull/123',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

