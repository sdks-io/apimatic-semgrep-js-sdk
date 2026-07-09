
# Rule

*This model accepts additional fields of type unknown.*

## Structure

`Rule`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | `string \| undefined` | Optional | Category the Rule is associated with. |
| `confidence` | [`Confidence \| undefined`](../../doc/models/confidence.md) | Optional | Confidence based on the Rule's false-positive rate.<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| CONFIDENCE_HIGH \|  \|<br>\| CONFIDENCE_MEDIUM \|  \|<br>\| CONFIDENCE_LOW \|  \| |
| `cweCategories` | `string[] \| undefined` | Optional | The CWE associated with the Rule. |
| `hasValidators` | `boolean \| undefined` | Optional | When True, the secrets rule has validators. |
| `id` | `string \| undefined` | Optional | ID of the Rule. |
| `languages` | `string[] \| undefined` | Optional | Languages the Rule applies to. |
| `lastChangeAt` | `string \| undefined` | Optional | Timestamp of when the Rule was last changed. |
| `lastChangeBy` | `string \| undefined` | Optional | Username of who last changed the Rule. |
| `owaspCategories` | `string[] \| undefined` | Optional | Owasp categories the Rule is associated with. |
| `path` | `string \| undefined` | Optional | Full path of the Rule. |
| `policyMode` | [`PolicyMode \| undefined`](../../doc/models/policy-mode.md) | Optional | Mode behavior: Monitor / Comment / Block / Disabled<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| |
| `registryMaintainer` | `string \| undefined` | Optional | The Registry maintainer associated with the Rule (if applicable). |
| `rulesets` | `string[] \| undefined` | Optional | Rulesets to which the Rule belongs (if applicable). |
| `secretType` | `string \| undefined` | Optional | The secret type (if applicable). |
| `severity` | [`Severity \| undefined`](../../doc/models/severity.md) | Optional | Severity level ("seriousness" of the finding)<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SEVERITY_HIGH \|  \|<br>\| SEVERITY_MEDIUM \|  \|<br>\| SEVERITY_LOW \|  \|<br>\| SEVERITY_CRITICAL \|  \| |
| `source` | [`Source \| undefined`](../../doc/models/source.md) | Optional | Source of the Rule<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| SOURCE_PRO \| From Pro rules \|<br>\| SOURCE_COMMUNITY \| From Semgrep Community rules \|<br>\| SOURCE_CUSTOM \| From Custom rules \| |
| `technologies` | `string[] \| undefined` | Optional | Technologies the Rule is associated with. |
| `url` | `string \| undefined` | Optional | The URL of the Rule. |
| `vulnerabilityClass` | `string[] \| undefined` | Optional | Vulnerability classes the Rule is associated with. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  Confidence,
  PolicyMode,
  Rule,
  Severity,
  Source,
} from 'apimatic-semgrep-sdk';

const rule: Rule = {
  category: 'security',
  confidence: Confidence.ConfidenceHigh,
  cweCategories: [
    'CWE-918: Server-Side Request Forgery (SSRF)'
  ],
  hasValidators: false,
  id: 'id0',
  languages: [
    'python'
  ],
  lastChangeAt: '2024-07-29 22:33:37.380293+00:00',
  owaspCategories: [
    'A07: Cross-Site Scripting (XSS)'
  ],
  path: 'python.rule.1',
  policyMode: PolicyMode.ModeBlock,
  registryMaintainer: 'semgrep',
  rulesets: [],
  severity: Severity.SeverityHigh,
  source: Source.SourceCommunity,
  technologies: [
    'django',
    'flask'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

