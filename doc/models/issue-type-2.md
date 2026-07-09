
# Issue Type 2

Type of findings to return. If not specified, returns `sast` (Code) findings. Can be `sast` (Code), `sca` (Supply Chain), or `ai_sast` (AI-powered scan). Valid values: sast, sca, ai_sast

## Enumeration

`IssueType2`

## Fields

| Name |
|  --- |
| `Sast` |
| `Sca` |
| `AiSast` |

## Example

```ts
import { IssueType2 } from 'apimatic-semgrep-sdk';

const issueType2 = IssueType2.Sca;
```

