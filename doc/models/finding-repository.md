
# Finding Repository

Which repository this finding was identified in

*This model accepts additional fields of type unknown.*

## Structure

`FindingRepository`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | The repository or named project that the finding is associated with |
| `url` | `string \| undefined` | Optional | The source URL from which this repository last scanned |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { FindingRepository } from 'apimatic-semgrep-sdk';

const findingRepository: FindingRepository = {
  name: 'semgrep',
  url: 'https://github.com/semgrep/semgrep',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

