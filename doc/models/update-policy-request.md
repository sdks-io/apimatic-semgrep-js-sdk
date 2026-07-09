
# Update Policy Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdatePolicyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Required | Deployment ID (numeric). Example: `123`. Can be found at `/deployments`, or in your Settings in the web UI. |
| `policyId` | `string` | Required | Policy ID (numeric). Example: `456`. Can be found at `/deployments/{deploymentId}/policies`. |
| `policyMode` | [`PolicyMode3`](../../doc/models/policy-mode-3.md) | Required | New policy mode to set for the Rule.<br><br>- MODE_MONITOR: Monitor mode, silently report findings<br>- MODE_COMMENT: Comment mode, leaves PR comments but does not block<br>- MODE_BLOCK: Block mode, leaves PR comments and blocks PR<br>- MODE_DISABLED: Disabled mode, not active<br><br>\| value \| description \|<br>\|-------\|---------------\|<br>\| MODE_MONITOR \| Monitor mode, silently report findings \|<br>\| MODE_COMMENT \| Comment mode, leaves PR comments but does not block \|<br>\| MODE_BLOCK \| Block mode, leaves PR comments and blocks PR \|<br>\| MODE_DISABLED \| Disabled mode, not active \| |
| `rulePath` | `string` | Required | Full path of the Rule. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { PolicyMode3, UpdatePolicyRequest } from 'apimatic-semgrep-sdk';

const updatePolicyRequest: UpdatePolicyRequest = {
  deploymentId: '123',
  policyId: '456',
  policyMode: PolicyMode3.ModeMonitor,
  rulePath: 'rulePath2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

