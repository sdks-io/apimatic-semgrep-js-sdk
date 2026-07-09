
# List Findings Response

Response containing a paginated list of findings (either Code or Supply Chain findings) with optional filtering applied

*This model accepts additional fields of type unknown.*

## Structure

`ListFindingsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `aiSastFindings` | [`AiSastFindings \| undefined`](../../doc/models/ai-sast-findings.md) | Optional | A list of AI-powered scan findings that Semgrep has identified in your organization |
| `sastFindings` | [`SastFindings \| undefined`](../../doc/models/sast-findings.md) | Optional | A list of Code findings that Semgrep has identified in your organization |
| `scaFindings` | [`ScaFindings \| undefined`](../../doc/models/sca-findings.md) | Optional | A list of Supply Chain findings that Semgrep has identified in your organization |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence1,
  ListFindingsResponse,
  Risk,
  Verdict1,
} from 'apimatic-semgrep-sdk';

const listFindingsResponse: ListFindingsResponse = {
  aiSastFindings: {
    findings: [
      {
        aiImpact: 'ai_impact2',
        assistant: {
          autofix: {
            explanation: 'explanation2',
            fixCode: 'fix_code4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          autotriage: {
            reason: 'reason2',
            verdict: Verdict1.FalsePositive,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          component: {
            risk: Risk.High,
            tag: 'tag8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          guidance: {
            instructions: 'instructions4',
            summary: 'summary8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          ruleExplanation: {
            explanation: 'explanation8',
            summary: 'summary4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        clickToFixFailures: [
          {
            createdAt: 'created_at8',
            reason: 'reason0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        clickToFixPrs: [
          {
            createdAt: 'created_at4',
            url: 'url0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        confidence: Confidence1.Low,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        aiImpact: 'ai_impact2',
        assistant: {
          autofix: {
            explanation: 'explanation2',
            fixCode: 'fix_code4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          autotriage: {
            reason: 'reason2',
            verdict: Verdict1.FalsePositive,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          component: {
            risk: Risk.High,
            tag: 'tag8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          guidance: {
            instructions: 'instructions4',
            summary: 'summary8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          ruleExplanation: {
            explanation: 'explanation8',
            summary: 'summary4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        clickToFixFailures: [
          {
            createdAt: 'created_at8',
            reason: 'reason0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        clickToFixPrs: [
          {
            createdAt: 'created_at4',
            url: 'url0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        confidence: Confidence1.Low,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        aiImpact: 'ai_impact2',
        assistant: {
          autofix: {
            explanation: 'explanation2',
            fixCode: 'fix_code4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          autotriage: {
            reason: 'reason2',
            verdict: Verdict1.FalsePositive,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          component: {
            risk: Risk.High,
            tag: 'tag8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          guidance: {
            instructions: 'instructions4',
            summary: 'summary8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          ruleExplanation: {
            explanation: 'explanation8',
            summary: 'summary4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        clickToFixFailures: [
          {
            createdAt: 'created_at8',
            reason: 'reason0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        clickToFixPrs: [
          {
            createdAt: 'created_at4',
            url: 'url0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        confidence: Confidence1.Low,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  sastFindings: {
    findings: [
      {
        assistant: {
          autofix: {
            explanation: 'explanation2',
            fixCode: 'fix_code4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          autotriage: {
            reason: 'reason2',
            verdict: Verdict1.FalsePositive,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          component: {
            risk: Risk.High,
            tag: 'tag8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          guidance: {
            instructions: 'instructions4',
            summary: 'summary8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          ruleExplanation: {
            explanation: 'explanation8',
            summary: 'summary4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        categories: [
          'categories4',
          'categories3'
        ],
        clickToFixFailures: [
          {
            createdAt: 'created_at8',
            reason: 'reason0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        clickToFixPrs: [
          {
            createdAt: 'created_at4',
            url: 'url0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        confidence: Confidence1.Low,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        assistant: {
          autofix: {
            explanation: 'explanation2',
            fixCode: 'fix_code4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          autotriage: {
            reason: 'reason2',
            verdict: Verdict1.FalsePositive,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          component: {
            risk: Risk.High,
            tag: 'tag8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          guidance: {
            instructions: 'instructions4',
            summary: 'summary8',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          ruleExplanation: {
            explanation: 'explanation8',
            summary: 'summary4',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        categories: [
          'categories4',
          'categories3'
        ],
        clickToFixFailures: [
          {
            createdAt: 'created_at8',
            reason: 'reason0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        clickToFixPrs: [
          {
            createdAt: 'created_at4',
            url: 'url0',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        confidence: Confidence1.Low,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  scaFindings: {
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
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

