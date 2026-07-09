
# Transitivities 2

List of transitivities to filter by. If not specified, returns all transitivities. This filter is applicable when `issue_type=sca` is specified. Valid values: direct, transitive, unknown

## Enumeration

`Transitivities2`

## Fields

| Name |
|  --- |
| `Direct` |
| `Transitive` |
| `Unknown` |

## Example

```ts
import { Transitivities2 } from 'apimatic-semgrep-sdk';

const transitivities2 = Transitivities2.Direct;
```

