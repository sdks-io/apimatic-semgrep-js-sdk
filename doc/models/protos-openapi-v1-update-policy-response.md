
# Protos Openapi V1 Update Policy Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1UpdatePolicyResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `policyId` | `string \| undefined` | Optional | Policy ID (numeric). Example: `456`. Can be found at `/deployments/{deploymentId}/policies`. |
| `updatedRule` | [`Rule \| undefined`](../../doc/models/rule.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence,
  ProtosOpenapiV1UpdatePolicyResponse,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1UpdatePolicyResponse: ProtosOpenapiV1UpdatePolicyResponse = {
  policyId: '1',
  updatedRule: {
    category: 'category4',
    confidence: Confidence.ConfidenceHigh,
    cweCategories: [
      'cweCategories9'
    ],
    hasValidators: false,
    id: 'id6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

