
# Click to Fix Failure

A failed PR creation attempt by Semgrep's Click to Fix feature

*This model accepts additional fields of type unknown.*

## Structure

`ClickToFixFailure`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `createdAt` | `string \| undefined` | Optional | When this failure occurred |
| `reason` | `string \| undefined` | Optional | Reason for the PR creation failure |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ClickToFixFailure } from 'apimatic-semgrep-sdk';

const clickToFixFailure: ClickToFixFailure = {
  createdAt: '2024-01-15 10:30:00+00:00',
  reason: 'merge conflict in target branch',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

