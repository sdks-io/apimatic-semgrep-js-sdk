
# Deployment

Deployment record, with relevant meta-data and further accesses.

*This model accepts additional fields of type unknown.*

## Structure

`Deployment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `findings` | [`EndpointReference \| undefined`](../../doc/models/endpoint-reference.md) | Optional | - |
| `id` | `bigint` | Required | Unique numerical identifier of the deployment. |
| `name` | `string` | Required | Human readable name. |
| `slug` | `string` | Required | Sanitized machine-readable name. Used as primary identifier through the web API. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Deployment } from 'apimatic-semgrep-sdk';

const deployment: Deployment = {
  id: BigInt(120),
  name: 'Your Deployment',
  slug: 'your-deployment',
  findings: {
    url: 'url2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

