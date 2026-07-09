
# Policy

*This model accepts additional fields of type unknown.*

## Structure

`Policy`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | ID of the Policy. |
| `isDefault` | `boolean \| undefined` | Optional | When True, the Policy applies to all repositories. |
| `name` | `string \| undefined` | Optional | Name of the Policy. |
| `productType` | [`ProductType \| undefined`](../../doc/models/product-type.md) | Optional | Product type the Policy applies to.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| PRODUCT_TYPE_SAST \| The product type for Code rules. \|<br>\| PRODUCT_TYPE_SECRETS \| The product type for Secrets rules. \| |
| `slug` | `string \| undefined` | Optional | Sanitized machine-readable name of the Policy. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Policy, ProductType } from 'apimatic-semgrep-sdk';

const policy: Policy = {
  id: '1',
  isDefault: true,
  name: 'Global Policy',
  productType: ProductType.ProductTypeSast,
  slug: 'global_policy',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

