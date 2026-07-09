
# Fix Recommendation

Recommendation for fixing the vulnerability

*This model accepts additional fields of type unknown.*

## Structure

`FixRecommendation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mPackage` | `string \| undefined` | Optional | The package for which a fix is recommended |
| `version` | `string \| undefined` | Optional | The recommended version of the package |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { FixRecommendation } from 'apimatic-semgrep-sdk';

const fixRecommendation: FixRecommendation = {
  mPackage: 'System.Drawing.Common',
  version: '5.0.3',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

