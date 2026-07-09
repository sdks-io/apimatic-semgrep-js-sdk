
# Protos Openapi V1 Get Bootstrap Sms Vpc Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1GetBootstrapSmsVpcResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `awsTemplateFormatVersion` | `string \| undefined` | Optional | The AWSTemplateFormatVersion that the template conforms to |
| `description` | `string \| undefined` | Optional | Template description |
| `metadata` | `unknown \| undefined` | Optional | Template metadata including version and last updated date |
| `outputs` | `unknown \| undefined` | Optional | Output values of the stack |
| `parameters` | `unknown \| undefined` | Optional | Template parameters |
| `resources` | `unknown \| undefined` | Optional | Declaration of AWS resources |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ProtosOpenapiV1GetBootstrapSmsVpcResponse,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1GetBootstrapSmsVpcResponse: ProtosOpenapiV1GetBootstrapSmsVpcResponse = {
  awsTemplateFormatVersion: 'AWSTemplateFormatVersion0',
  description: 'Description8',
  metadata: { 'key1': 'val1', 'key2': 'val2' },
  outputs: { 'key1': 'val1', 'key2': 'val2' },
  parameters: { 'key1': 'val1', 'key2': 'val2' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

