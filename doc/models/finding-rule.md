
# Finding Rule

Rule that applies to this finding

*This model accepts additional fields of type unknown.*

## Structure

`FindingRule`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | `string \| undefined` | Optional | Category the rule is associated with |
| `confidence` | [`Confidence2 \| undefined`](../../doc/models/confidence-2.md) | Optional | Confidence level of the rule |
| `cweNames` | `string[] \| undefined` | Optional | CWE names associated with the rule |
| `message` | `string \| undefined` | Optional | Rule message |
| `name` | `string \| undefined` | Optional | Name of the rule |
| `owaspNames` | `string[] \| undefined` | Optional | OWASP names associated with the rule |
| `subcategories` | `string[] \| undefined` | Optional | Subcategories of the rule |
| `vulnerabilityClasses` | `string[] \| undefined` | Optional | Vulnerability classes the rule is associated with |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Confidence2, FindingRule } from 'apimatic-semgrep-sdk';

const findingRule: FindingRule = {
  category: 'security',
  confidence: Confidence2.High,
  cweNames: [
    'CWE-319: Cleartext Transmission of Sensitive Information'
  ],
  message: 'This link points to a plaintext HTTP URL. Prefer an encrypted HTTPS URL if possible.',
  name: 'html.security.plaintext-http-link.plaintext-http-link',
  owaspNames: [
    'A03:2017 - Sensitive Data Exposure',
    'A02:2021 - Cryptographic Failures'
  ],
  subcategories: [
    'vuln'
  ],
  vulnerabilityClasses: [
    'Mishandled Sensitive Information'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

