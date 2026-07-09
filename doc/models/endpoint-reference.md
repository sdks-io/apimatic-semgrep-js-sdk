
# Endpoint Reference

*This model accepts additional fields of type unknown.*

## Structure

`EndpointReference`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `string` | Required | URL that the reference is pointing to. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { EndpointReference } from 'apimatic-semgrep-sdk';

const endpointReference: EndpointReference = {
  url: 'https://semgrep.dev/api/v1/deployments/123/findings',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

