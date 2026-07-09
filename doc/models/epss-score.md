
# Epss Score

The score assigned by FIRST.org's Exploitation Probability Scoring System

*This model accepts additional fields of type unknown.*

## Structure

`EpssScore`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percentile` | `number \| undefined` | Optional | This EPSS score's percentile among all EPSS scores, from 0 to 1 |
| `score` | `number \| undefined` | Optional | The explotation probability, from 0 to 1 |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { EpssScore } from 'apimatic-semgrep-sdk';

const epssScore: EpssScore = {
  percentile: 0.994,
  score: 0.97,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

