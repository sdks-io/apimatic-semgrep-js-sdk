
# Status

The finding's status as exposed in the UI. Status is a derived property combining information from the finding `state` and `triage_state`. The `triage_state` can be used to override the scan state if the finding is still detected

## Enumeration

`Status`

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
import { Status } from 'apimatic-semgrep-sdk';

const status = Status.Ignored;
```

