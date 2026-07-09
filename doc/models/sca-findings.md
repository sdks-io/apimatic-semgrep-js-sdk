
# Sca Findings

A list of Supply Chain findings that Semgrep has identified in your organization

*This model accepts additional fields of type unknown.*

## Structure

`ScaFindings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `findings` | [`ScaFinding[] \| undefined`](../../doc/models/sca-finding.md) | Optional | A list of Supply Chain findings. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Confidence1, ScaFindings } from 'apimatic-semgrep-sdk';

const scaFindings: ScaFindings = {
  findings: [
    {
      categories: [
        'categories4',
        'categories3'
      ],
      confidence: Confidence1.Low,
      createdAt: 'created_at6',
      epssScore: {
        percentile: 236.52,
        score: 242.58,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      externalTicket: {
        externalSlug: 'external_slug4',
        id: BigInt(228),
        linkedIssueIds: [
          BigInt(115),
          BigInt(116),
          BigInt(117)
        ],
        url: 'url8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      categories: [
        'categories4',
        'categories3'
      ],
      confidence: Confidence1.Low,
      createdAt: 'created_at6',
      epssScore: {
        percentile: 236.52,
        score: 242.58,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      externalTicket: {
        externalSlug: 'external_slug4',
        id: BigInt(228),
        linkedIssueIds: [
          BigInt(115),
          BigInt(116),
          BigInt(117)
        ],
        url: 'url8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      categories: [
        'categories4',
        'categories3'
      ],
      confidence: Confidence1.Low,
      createdAt: 'created_at6',
      epssScore: {
        percentile: 236.52,
        score: 242.58,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      externalTicket: {
        externalSlug: 'external_slug4',
        id: BigInt(228),
        linkedIssueIds: [
          BigInt(115),
          BigInt(116),
          BigInt(117)
        ],
        url: 'url8',
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

