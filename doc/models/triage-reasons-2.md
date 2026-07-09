
# Triage Reasons 2

Which triage reasons do you want to include? If not specified, includes all. This filter is applicable when `status` is `ignored`. Valid values: acceptable_risk, false_positive, no_time, no_triage_reason, duplicate

## Enumeration

`TriageReasons2`

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
import { TriageReasons2 } from 'apimatic-semgrep-sdk';

const triageReasons2 = TriageReasons2.FalsePositive;
```

