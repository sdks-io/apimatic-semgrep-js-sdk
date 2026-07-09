
# Rule Explanation

AI-generated explanation of why a rule flagged this specific code

*This model accepts additional fields of type unknown.*

## Structure

`RuleExplanation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `explanation` | `string \| undefined` | Optional | Detailed explanation of why this rule flagged the code, including context about the security issue and why it applies to this specific code. AI generated content, review carefully |
| `summary` | `string \| undefined` | Optional | A concise summary of the rule explanation. May not be present for all findings |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { RuleExplanation } from 'apimatic-semgrep-sdk';

const ruleExplanation: RuleExplanation = {
  explanation: 'This code is vulnerable to SQL injection because user input from the `username` parameter is directly concatenated into the SQL query string without sanitization or parameterization.',
  summary: 'User input directly concatenated into SQL query',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

