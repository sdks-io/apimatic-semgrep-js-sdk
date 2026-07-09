
# New Triage State

The triage state you would like to bulk triage your findings to.

## Enumeration

`NewTriageState`

## Fields

| Name |
|  --- |
| `Ignored` |
| `Reviewing` |
| `Fixing` |
| `Reopened` |
| `ProvisionallyIgnored` |

## Example

```ts
import { NewTriageState } from 'apimatic-semgrep-sdk';

const newTriageState = NewTriageState.ProvisionallyIgnored;
```

