
# Protos Openapi V1 List Policies Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1ListPoliciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `policies` | [`Policy[] \| undefined`](../../doc/models/policy.md) | Optional | List of Policies associated with the given Deployment. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ProductType,
  ProtosOpenapiV1ListPoliciesResponse,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1ListPoliciesResponse: ProtosOpenapiV1ListPoliciesResponse = {
  policies: [
    {
      id: '1',
      isDefault: true,
      name: 'Global Policy',
      productType: ProductType.ProductTypeSast,
      slug: 'global_policy',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: '2',
      isDefault: false,
      name: 'Semgrep test',
      productType: ProductType.ProductTypeSast,
      slug: 'semgrep_test',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: '3',
      isDefault: true,
      name: 'Global Secrets Policy',
      productType: ProductType.ProductTypeSecrets,
      slug: 'global_secrets_policy',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

