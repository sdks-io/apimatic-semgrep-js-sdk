
# Api V1 Deployments Findings Response Findings

## Class Name

`ApiV1DeploymentsFindingsResponseFindings`

## Cases

| Type |
|  --- |
| [`SastFinding`](../../../doc/models/sast-finding.md) |
| [`ScaFinding`](../../../doc/models/sca-finding.md) |
| [`AiPoweredScanFinding`](../../../doc/models/ai-powered-scan-finding.md) |

## SastFinding

### Initialization Code

#### Example

```ts
const value: ApiV1DeploymentsFindingsResponseFindings = {
  categories: [
    'security'
  ],
  confidence: Confidence1.Medium,
  createdAt: '2020-11-18 23:28:12.391807+00:00',
  firstSeenScanId: BigInt(1234),
  id: BigInt(1234567),
  lineOfCodeUrl: 'https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1',
  matchBasedId: '0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1',
  ref: 'refs/pull/1234/merge',
  relevantSince: '2020-11-18 23:28:12.391807+00:00',
  ruleName: 'typescript.react.security.audit.react-no-refs.react-no-refs',
  severity: Severity1.Medium,
  state: State.Unresolved,
  stateUpdatedAt: '2020-11-19 23:28:12.391807+00:00',
  status: Status.Open,
  syntacticId: '440eeface888e78afceac3dc7d4cc2cf',
  triageComment: 'This finding is from the test repo',
  triageReason: TriageReason.AcceptableRisk,
  triageState: TriageState.Untriaged,
  triagedAt: '2020-11-19 23:28:12.391807+00:00',
};
```

## ScaFinding

### Initialization Code

#### Example

```ts
const value: ApiV1DeploymentsFindingsResponseFindings = {
  categories: [
    'security'
  ],
  confidence: Confidence1.Medium,
  createdAt: '2020-11-18 23:28:12.391807+00:00',
  firstSeenScanId: BigInt(1234),
  id: BigInt(1234567),
  isMalicious: true,
  lineOfCodeUrl: 'https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1',
  matchBasedId: '0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1',
  reachability: Reachability.Reachable,
  reachableCondition: 'you use the package on a host running Linux or MacOS',
  ref: 'refs/pull/1234/merge',
  relevantSince: '2020-11-18 23:28:12.391807+00:00',
  ruleName: 'typescript.react.security.audit.react-no-refs.react-no-refs',
  severity: Severity1.Medium,
  state: State.Unresolved,
  stateUpdatedAt: '2020-11-19 23:28:12.391807+00:00',
  status: Status.Open,
  syntacticId: '440eeface888e78afceac3dc7d4cc2cf',
  triageComment: 'This finding is from the test repo',
  triageReason: TriageReason.AcceptableRisk,
  triageState: TriageState.Untriaged,
  triagedAt: '2020-11-19 23:28:12.391807+00:00',
  vulnerabilityIdentifier: 'CVE-2021-24112',
};
```

## AiPoweredScanFinding

### Initialization Code

#### Example

```ts
const value: ApiV1DeploymentsFindingsResponseFindings = {
  aiImpact: 'An attacker could access or modify other users\' data by manipulating the resource identifier in the request',
  confidence: Confidence1.Medium,
  createdAt: '2020-11-18 23:28:12.391807+00:00',
  firstSeenScanId: BigInt(1234),
  id: BigInt(1234567),
  lineOfCodeUrl: 'https://github.com/semgrep/semgrep/blob/39f95450a7d4d70e54c9edbd109bed8210a36889/src/core_cli/Core_CLI.ml#L1',
  matchBasedId: '0f8c79a6f7e0ff2f908ff5bc366ae1548465069bae8892088051e1c3b4b12c6b8df37d5bcbb181eb868aa79f81f239d14bf2336d552786ab8ccdc7279adf07a6_1',
  ref: 'refs/pull/1234/merge',
  relevantSince: '2020-11-18 23:28:12.391807+00:00',
  ruleName: 'ai.detection.idor',
  severity: Severity1.High,
  state: State.Unresolved,
  stateUpdatedAt: '2020-11-19 23:28:12.391807+00:00',
  status: Status.Open,
  syntacticId: '440eeface888e78afceac3dc7d4cc2cf',
  triageComment: 'This finding is from the test repo',
  triageReason: TriageReason.AcceptableRisk,
  triageState: TriageState.Untriaged,
  triagedAt: '2020-11-19 23:28:12.391807+00:00',
};
```

