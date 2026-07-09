
# Policy Reference

Reference to a policy, with some basic information. If null, then the information does not exist or lacks integrity (older or broken scans)

*This model accepts additional fields of type unknown.*

## Structure

`PolicyReference`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `bigint \| undefined` | Optional | Unique numerical identifier of the policy |
| `name` | `string \| undefined` | Optional | Human readable name |
| `slug` | `string \| undefined` | Optional | Sanitized machine-readable name |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { PolicyReference } from 'apimatic-semgrep-sdk';

const policyReference: PolicyReference = {
  id: BigInt(120),
  name: 'Default Policy',
  slug: 'default-policy',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

