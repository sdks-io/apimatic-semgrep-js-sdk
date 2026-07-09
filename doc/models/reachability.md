
# Reachability

Indicates whether the vulnerable code is reachable

## Enumeration

`Reachability`

## Fields

| Name |
|  --- |
| `EnumNoReachabilityAnalysis` |
| `Reachable` |
| `EnumAlwaysReachable` |
| `EnumConditionallyReachable` |
| `Unreachable` |

## Example

```ts
import { Reachability } from 'apimatic-semgrep-sdk';

const reachability = Reachability.EnumNoReachabilityAnalysis;
```

