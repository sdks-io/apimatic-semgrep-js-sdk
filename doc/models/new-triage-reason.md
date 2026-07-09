
# New Triage Reason

The reason for triaging to a given triage state.

## Enumeration

`NewTriageReason`

## Fields

| Name |
|  --- |
| `AcceptableRisk` |
| `FalsePositive` |
| `NoTime` |
| `NoTriageReason` |
| `Duplicate` |

## Example

```ts
import { NewTriageReason } from 'apimatic-semgrep-sdk';

const newTriageReason = NewTriageReason.FalsePositive;
```

