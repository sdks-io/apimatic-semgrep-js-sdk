
# Float Range

*This model accepts additional fields of type unknown.*

## Structure

`FloatRange`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `max` | `number \| undefined` | Optional | End of the range |
| `min` | `number \| undefined` | Optional | Start of the range |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { FloatRange } from 'apimatic-semgrep-sdk';

const floatRange: FloatRange = {
  max: 69.02,
  min: 4.4,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

