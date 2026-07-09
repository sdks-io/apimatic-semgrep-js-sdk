# Triage Service

View and manage the triage of your organization.

```ts
const triageServiceApi = new TriageServiceApi(client);
```

## Class Name

`TriageServiceApi`


# Bulk Triage

Bulk triage your findings. You can select the findings to triage by passing in a list of finding IDs as issue_ids, or by passing in filter query parameters. You must specify the issue_type of the findings you want to bulk triage. One of new_triage_state or new_note is required. If specifying a new_triage_reason, you must also use new_triage_state=ignored. Some filters only apply for findings associated with a given product.

```ts
async bulkTriage(
  deploymentSlug: string,
  body: BulkTriageRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<BulkTriageResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `body` | [`BulkTriageRequest`](../../doc/models/bulk-triage-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`BulkTriageResponse`](../../doc/models/bulk-triage-response.md).

## Example Usage

```ts
const deploymentSlug = 'deploymentSlug6';

const body: BulkTriageRequest = {
  issueType: IssueType.Sca,
  autotriageVerdict: AutotriageVerdict.TruePositive,
  categories: [
    'security',
    'performance'
  ],
  componentTags: [
    'user authentication',
    'user data'
  ],
  confidence: Confidence3.High,
  dependencies: [
    'lodash',
    'express'
  ],
  includeHistorical: true,
  issueIds: [
    BigInt(123),
    BigInt(456)
  ],
  limit: BigInt(100),
  newNote: 'some note here',
  newTriageReason: NewTriageReason.AcceptableRisk,
  newTriageState: NewTriageState.Reopened,
  policies: [
    'rule-board-block',
    'rule-board-pr-comments',
    'rule-board-audit'
  ],
  proOnly: true,
  projectTags: [
    'my_project_tag_1',
    'my_project_tag_2'
  ],
  ref: 'refs/pull/1234/merge',
  repos: [
    'myorg/repo1',
    'myorg/repo2'
  ],
  rules: [
    'typescript.react.security.audit.react-no-refs.react-no-refs',
    'ajinabraham.njsscan.hardcoded_secrets.node_username'
  ],
  ruleset: [
    'owasp-top-ten',
    'default'
  ],
  secretTypes: [
    'Github',
    'Heroku',
    'AWS'
  ],
  since: '1717334400',
  status: Status1.Open,
};

try {
  const response = await triageServiceApi.bulkTriage(
    deploymentSlug,
    body
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

