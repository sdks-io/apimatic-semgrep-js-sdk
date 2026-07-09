
# Protos Openapi V1 List Policy Rules Response

*This model accepts additional fields of type unknown.*

## Structure

`ProtosOpenapiV1ListPolicyRulesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Cursor to paginate through the rules. |
| `policy` | [`Policy \| undefined`](../../doc/models/policy.md) | Optional | - |
| `rules` | [`Rule[] \| undefined`](../../doc/models/rule.md) | Optional | List of Rules for the given Policy. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence,
  PolicyMode,
  ProductType,
  ProtosOpenapiV1ListPolicyRulesResponse,
  Severity,
  Source,
} from 'apimatic-semgrep-sdk';

const protosOpenapiV1ListPolicyRulesResponse: ProtosOpenapiV1ListPolicyRulesResponse = {
  cursor: 'Pm0ROjIwMjQtMDItMDYgMjA6MDQ6NDguMEDzNzk2fmk6NYTM2zUxOTI',
  policy: {
    id: 'id4',
    isDefault: false,
    name: 'name4',
    productType: ProductType.ProductTypeSast,
    slug: 'slug8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  rules: [
    {
      category: 'security',
      confidence: Confidence.ConfidenceHigh,
      cweCategories: [
        'CWE-918: Server-Side Request Forgery (SSRF)'
      ],
      hasValidators: false,
      id: '1',
      languages: [
        'python'
      ],
      lastChangeAt: '2024-07-29T22:33:37.380293Z',
      owaspCategories: [
        'A07: Cross-Site Scripting (XSS)'
      ],
      path: 'python.rule.1',
      policyMode: PolicyMode.ModeMonitor,
      registryMaintainer: 'semgrep',
      rulesets: [],
      severity: Severity.SeverityHigh,
      source: Source.SourceCommunity,
      technologies: [
        'django',
        'flask'
      ],
      url: 'https://semgrep.com/r/123/python.rule.1',
      vulnerabilityClass: [
        'Improper Authentication'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      category: 'security',
      confidence: Confidence.ConfidenceHigh,
      cweCategories: [
        'CWE-918: Server-Side Request Forgery (SSRF)'
      ],
      hasValidators: false,
      id: '2',
      languages: [
        'python'
      ],
      lastChangeAt: '2024-07-29T22:33:37.380293Z',
      owaspCategories: [
        'A01:2021 - Broken Access Control',
        'A07: Cross-Site Scripting (XSS)'
      ],
      path: 'python.rule.shared',
      policyMode: PolicyMode.ModeComment,
      registryMaintainer: 'semgrep',
      rulesets: [
        'comment',
        'default'
      ],
      severity: Severity.SeverityMedium,
      source: Source.SourcePro,
      technologies: [
        'django',
        'flask'
      ],
      url: 'https://semgrep.com/r/123/python.rule.shared',
      vulnerabilityClass: [
        'Improper Authentication'
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      category: 'best-practice',
      confidence: Confidence.ConfidenceHigh,
      cweCategories: [],
      hasValidators: false,
      id: '3',
      languages: [
        'python'
      ],
      lastChangeAt: '2024-07-29T22:33:37.380293Z',
      lastChangeBy: 'example-user',
      owaspCategories: [],
      path: 'python.rule.custom_rule',
      policyMode: PolicyMode.ModeBlock,
      registryMaintainer: 'semgrep',
      rulesets: [],
      severity: Severity.SeverityMedium,
      source: Source.SourceCustom,
      technologies: [
        'django',
        'flask'
      ],
      url: 'https://semgrep.com/r/123/python.rule.custom_rule',
      vulnerabilityClass: [
        'Improper Authentication'
      ],
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

