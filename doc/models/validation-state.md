
# Validation State

Filter by whether a secret could be validated. Only applies for secrets findings.

## Enumeration

`ValidationState`

## Fields

| Name |
|  --- |
| `ConfirmedValid` |
| `ConfirmedInvalid` |
| `ValidationError` |
| `NoValidator` |

## Example

```ts
import { ValidationState } from 'apimatic-semgrep-sdk';

const validationState = ValidationState.ValidationError;
```

