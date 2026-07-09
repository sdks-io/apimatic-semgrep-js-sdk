
# Protos Openapi V1 List Deployments Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1ListDeploymentsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deployments` | [`Deployment[] \| undefined`](../../doc/models/deployment.md) | Optional | Return the deployment the supplied token can access. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosOpenapiV1ListDeploymentsResponse } from 'apimatic-semgrep-sdk';

const protosOpenapiV1ListDeploymentsResponse: ProtosOpenapiV1ListDeploymentsResponse = {
  deployments: [
    {
      id: BigInt(106),
      name: 'name6',
      slug: 'slug0',
      findings: {
        url: 'url2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      id: BigInt(106),
      name: 'name6',
      slug: 'slug0',
      findings: {
        url: 'url2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
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

