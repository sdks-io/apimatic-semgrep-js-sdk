
# Component

Semgrep Assistant's guess as for what the matched source code's purpose is

*This model accepts additional fields of type unknown.*

## Structure

`Component`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `risk` | [`Risk \| undefined`](../../doc/models/risk.md) | Optional | Component risk level |
| `tag` | `string \| undefined` | Optional | Component tag |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Component, Risk } from 'apimatic-semgrep-sdk';

const component: Component = {
  risk: Risk.High,
  tag: 'user data',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

