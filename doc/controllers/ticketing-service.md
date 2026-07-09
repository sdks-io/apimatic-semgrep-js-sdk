# Ticketing Service

Create and manage external tickets

```ts
const ticketingServiceApi = new TicketingServiceApi(client);
```

## Class Name

`TicketingServiceApi`

## Methods

* [Ticketing Service Delete Ticket](../../doc/controllers/ticketing-service.md#ticketing-service-delete-ticket)
* [Ticketing Service Link Ticket](../../doc/controllers/ticketing-service.md#ticketing-service-link-ticket)
* [Ticketing Service Unlink Ticket](../../doc/controllers/ticketing-service.md#ticketing-service-unlink-ticket)
* [Ticketing Service Create Ticket](../../doc/controllers/ticketing-service.md#ticketing-service-create-ticket)


# Ticketing Service Delete Ticket

Unlink a Jira ticket by its ID

```ts
async ticketingServiceDeleteTicket(
  deploymentId: string,
  externalTicketId: bigint,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1DeleteTicketResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `externalTicketId` | `bigint` | Template, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1DeleteTicketResponse`](../../doc/models/protos-openapi-v1-delete-ticket-response.md).

## Example Usage

```ts
const deploymentId = '123';

const externalTicketId = BigInt(456);

try {
  const response = await ticketingServiceApi.ticketingServiceDeleteTicket(
    deploymentId,
    externalTicketId
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


# Ticketing Service Link Ticket

Link an existing external ticket (e.g. Jira) to one or more Semgrep findings by providing the ticket URL and a list of finding IDs. This does not create a ticket in your issue tracker — it only records the association in Semgrep. If a finding is already linked to a different ticket, the existing link is replaced. Requires a configured ticketing integration.

```ts
async ticketingServiceLinkTicket(
  deploymentId: string,
  body: LinkTicketRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1LinkTicketResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`LinkTicketRequest`](../../doc/models/link-ticket-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1LinkTicketResponse`](../../doc/models/protos-openapi-v1-link-ticket-response.md).

## Example Usage

```ts
const deploymentId = '123';

const body: LinkTicketRequest = {
  deploymentId: '123',
  issueIds: [
    'issue_ids0',
    'issue_ids9'
  ],
  ticketUrl: 'https://myorg.atlassian.net/browse/SEC-123',
};

try {
  const response = await ticketingServiceApi.ticketingServiceLinkTicket(
    deploymentId,
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


# Ticketing Service Unlink Ticket

Remove the ticket association from one or more Semgrep findings by providing a list of finding IDs. This does not delete the ticket in your issue tracker — it only removes the association in Semgrep.

```ts
async ticketingServiceUnlinkTicket(
  deploymentId: string,
  body: UnlinkTicketRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1UnlinkTicketResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentId` | `string` | Template, Required | - |
| `body` | [`UnlinkTicketRequest`](../../doc/models/unlink-ticket-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1UnlinkTicketResponse`](../../doc/models/protos-openapi-v1-unlink-ticket-response.md).

## Example Usage

```ts
const deploymentId = '123';

const body: UnlinkTicketRequest = {
  deploymentId: '123',
  issueIds: [
    'issue_ids0',
    'issue_ids9'
  ],
};

try {
  const response = await ticketingServiceApi.ticketingServiceUnlinkTicket(
    deploymentId,
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


# Ticketing Service Create Ticket

Create Jira tickets for your findings. You can create tickets by passing in a list of issue_ids or by passing in filter query parameters to dynamically select findings. If passing in filters, Semgrep will skip already ticketed findings. This endpoint is synchronous, so it may take some time for your request to resolve. Unlike creating tickets in-app, if ticket creation fails we won't automatically retry. This endpoint accepts a limit parameter (defaulting to 20) to limit the number of tickets created per request. If you specify a list of issue_ids greater than this limit, or your selected filters match on a number of issues greater than this limit, issues that were not ticketed are included in the Failed part of the response object. You can send another request to create tickets for these skipped issues. By default, findings belonging to the same repository and the same rule will be grouped together into a single Jira ticket. You can override this using the group_issues query parameter. Up to 50 issues can be grouped into a single ticket. You can optionally override the Jira project you create tickets in by passing in a Jira project ID as jira_project_id (the numeric ID rather than the project key). You can fetch this ID using the Jira API.

```ts
async ticketingServiceCreateTicket(
  deploymentSlug: string,
  body: CreateTicketRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<ProtosOpenapiV1CreateTicketResponse>>
```

## Authentication

This endpoint requires [SemgrepWebToken](../../doc/auth/oauth-2-bearer-token-2.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deploymentSlug` | `string` | Template, Required | - |
| `body` | [`CreateTicketRequest`](../../doc/models/create-ticket-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`ProtosOpenapiV1CreateTicketResponse`](../../doc/models/protos-openapi-v1-create-ticket-response.md).

## Example Usage

```ts
const deploymentSlug = 'deploymentSlug6';

const body: CreateTicketRequest = {
  deploymentSlug: 'deploymentSlug2',
  issueType: IssueType1.Sca,
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
  groupIssues: true,
  includeHistorical: true,
  issueIds: [
    'issue_ids6',
    'issue_ids7'
  ],
  jiraProjectId: '12345',
  limit: BigInt(20),
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
  const response = await ticketingServiceApi.ticketingServiceCreateTicket(
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

