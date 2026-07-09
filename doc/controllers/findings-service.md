# Findings Service

Manage and retrieve code, supply chain, and AI-powered scan findings from Semgrep scans

```ts
const findingsServiceApi = new FindingsServiceApi(client);
```

## Class Name

`FindingsServiceApi`


# Findings Service List Findings

Request the list of code, supply chain, or AI-powered scan findings in an organization, paginated in pages of 100 entries and limited by the `since` timestamp. Findings are returned by `relevant_since` descending (see `since` in the Query Parameters list). Examples: List SAST findings with pagination, List SCA findings since timestamp, List AI-powered scan findings, List findings with filters.

```ts
async findingsServiceListFindings(
  deploymentSlug: string,
  issueType?: IssueType2,
  since?: number,
  page?: bigint,
  dedup?: boolean,
  pageSize?: bigint,
  repos?: string[],
  repositoryIds?: bigint[],
  status?: Status9,
  triageReasons?: TriageReasons2,
  severities?: Severities2,
  ref?: string,
  policies?: string[],
  rules?: string[],
  categories?: string[],
  confidence?: Confidence8,
  autotriageVerdict?: AutotriageVerdict2,
  componentTags?: string[],
  exposures?: Exposures2,
  transitivities?: Transitivities2,
  isMalicious?: boolean,
  clickToFixPrState?: ClickToFixPrState,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ApiV1DeploymentsFindingsResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `issueType` | [`IssueType2 \| undefined`](../../doc/models/issue-type-2.md) | Query, Optional | **Default**: `IssueType2.Sast` |
| `since` | `number \| undefined` | Query, Optional | - |
| `page` | `bigint \| undefined` | Query, Optional | **Default**: `0` |
| `dedup` | `boolean \| undefined` | Query, Optional | **Default**: `false` |
| `pageSize` | `bigint \| undefined` | Query, Optional | **Default**: `100`<br><br>**Constraints**: `>= 100`, `<= 3000` |
| `repos` | `string[] \| undefined` | Query, Optional | - |
| `repositoryIds` | `bigint[] \| undefined` | Query, Optional | - |
| `status` | [`Status9 \| undefined`](../../doc/models/status-9.md) | Query, Optional | - |
| `triageReasons` | [`TriageReasons2 \| undefined`](../../doc/models/triage-reasons-2.md) | Query, Optional | - |
| `severities` | [`Severities2 \| undefined`](../../doc/models/severities-2.md) | Query, Optional | - |
| `ref` | `string \| undefined` | Query, Optional | - |
| `policies` | `string[] \| undefined` | Query, Optional | - |
| `rules` | `string[] \| undefined` | Query, Optional | - |
| `categories` | `string[] \| undefined` | Query, Optional | - |
| `confidence` | [`Confidence8 \| undefined`](../../doc/models/confidence-8.md) | Query, Optional | - |
| `autotriageVerdict` | [`AutotriageVerdict2 \| undefined`](../../doc/models/autotriage-verdict-2.md) | Query, Optional | - |
| `componentTags` | `string[] \| undefined` | Query, Optional | - |
| `exposures` | [`Exposures2 \| undefined`](../../doc/models/exposures-2.md) | Query, Optional | - |
| `transitivities` | [`Transitivities2 \| undefined`](../../doc/models/transitivities-2.md) | Query, Optional | - |
| `isMalicious` | `boolean \| undefined` | Query, Optional | - |
| `clickToFixPrState` | [`ClickToFixPrState \| undefined`](../../doc/models/click-to-fix-pr-state.md) | Query, Optional | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ApiV1DeploymentsFindingsResponse`](../../doc/models/api-v1-deployments-findings-response.md).

## Example Usage

```ts
const deploymentSlug = 'your-deployment';

const issueType = IssueType2.Sca;

const since = 1636942398.45;

const page = BigInt(1);

const dedup = true;

const pageSize = BigInt(100);

const repos: string[] = [
  'myorg/repo1',
  'myorg/repo2'
];

const repositoryIds: bigint[] = [
  BigInt(1),
  BigInt(2),
  BigInt(3)
];

const status = Status9.Open;

const ref = 'refs/pull/1234/merge';

const policies: string[] = [
  'rule-board-block',
  'rule-board-pr-comments',
  'rule-board-audit'
];

const rules: string[] = [
  'typescript.react.security.audit.react-no-refs.react-no-refs',
  'ajinabraham.njsscan.hardcoded_secrets.node_username'
];

const categories: string[] = [
  'security',
  'correctness',
  'caching'
];

const confidence = Confidence8.High;

const autotriageVerdict = AutotriageVerdict2.TruePositive;

const componentTags: string[] = [
  'user authentication',
  'user data'
];

const isMalicious = true;

try {
  const response = await findingsServiceApi.findingsServiceListFindings(
    deploymentSlug,
    issueType,
    since,
    page,
    dedup,
    pageSize,
    repos,
    repositoryIds,
    status,
    undefined,
    undefined,
    ref,
    policies,
    rules,
    categories,
    confidence,
    autotriageVerdict,
    componentTags,
    undefined,
    undefined,
    isMalicious
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

