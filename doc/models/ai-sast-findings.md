
# Ai Sast Findings

A list of AI-powered scan findings that Semgrep has identified in your organization

*This model accepts additional fields of type unknown.*

## Structure

`AiSastFindings`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `findings` | [`AiPoweredScanFinding[] \| undefined`](../../doc/models/ai-powered-scan-finding.md) | Optional | A list of AI-powered scan findings. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  AiSastFindings,
  Confidence1,
  Risk,
  Verdict1,
} from 'apimatic-semgrep-sdk';

const aiSastFindings: AiSastFindings = {
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
};
```

