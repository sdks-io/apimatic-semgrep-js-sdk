
# Api V1 Deployments Findings Response

*This model accepts additional fields of type unknown.*

## Structure

`ApiV1DeploymentsFindingsResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `findings` | [`ApiV1DeploymentsFindingsResponseFindings[] \| undefined`](../../doc/models/containers/api-v1-deployments-findings-response-findings.md) | Optional | This is Array of a container for one-of cases. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  ApiV1DeploymentsFindingsResponse,
  Confidence1,
  Risk,
  Verdict1,
} from 'apimatic-semgrep-sdk';

const apiV1DeploymentsFindingsResponse: ApiV1DeploymentsFindingsResponse = {
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
        'categories4'
      ],
      clickToFixFailures: [
        {
          createdAt: 'created_at8',
          reason: 'reason0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          createdAt: 'created_at8',
          reason: 'reason0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
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
        },
        {
          createdAt: 'created_at4',
          url: 'url0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          createdAt: 'created_at4',
          url: 'url0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      confidence: Confidence1.High,
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
        'categories4'
      ],
      clickToFixFailures: [
        {
          createdAt: 'created_at8',
          reason: 'reason0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          createdAt: 'created_at8',
          reason: 'reason0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
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
        },
        {
          createdAt: 'created_at4',
          url: 'url0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          createdAt: 'created_at4',
          url: 'url0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      confidence: Confidence1.High,
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
        'categories4'
      ],
      clickToFixFailures: [
        {
          createdAt: 'created_at8',
          reason: 'reason0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          createdAt: 'created_at8',
          reason: 'reason0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
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
        },
        {
          createdAt: 'created_at4',
          url: 'url0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          createdAt: 'created_at4',
          url: 'url0',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      confidence: Confidence1.High,
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

