
# Protos Secrets V1 Historical Info

*This model accepts additional fields of type unknown.*

## Structure

`ProtosSecretsV1HistoricalInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `gitBlob` | `string \| undefined` | Optional | Git blob at which the finding is present. Sent in addition to the commit<br>since some SCMs have permalinks which use the blob sha, so this information<br>is useful when generating links back to the SCM. |
| `gitCommit` | `string \| undefined` | Optional | Git commit at which the finding is present. Used by "historical" scans,<br>which scan non-HEAD commits in the git history. Relevant for finding, e.g.,<br>secrets which are buried in the git history which we wouldn't find at HEAD |
| `gitCommitTimestamp` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProtosSecretsV1HistoricalInfo } from 'apimatic-semgrep-sdk';

const protosSecretsV1HistoricalInfo: ProtosSecretsV1HistoricalInfo = {
  gitBlob: 'gitBlob8',
  gitCommit: 'gitCommit2',
  gitCommitTimestamp: '2016-03-13T12:52:32.123Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

