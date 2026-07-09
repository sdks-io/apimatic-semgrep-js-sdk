
# Status 9

Which status do you want to include? If not specified, includes all statuses. Findings in the `removed` state are always excluded from this endpoint. Valid values: open, fixed, ignored, reviewing, fixing, provisionally_ignored

## Enumeration

`Status9`

## Fields

| Name |
|  --- |
| `Open` |
| `Fixed` |
| `Ignored` |
| `Reviewing` |
| `Fixing` |
| `ProvisionallyIgnored` |

## Example

```ts
import { Status9 } from 'apimatic-semgrep-sdk';

const status9 = Status9.Open;
```

