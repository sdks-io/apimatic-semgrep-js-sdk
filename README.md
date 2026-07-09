
# Getting Started with Semgrep Web App

## Introduction

Welcome to Semgrep's portal for the Semgrep AppSec Platform web API.

### Introduction

Semgrep is a fast, open-source, static analysis tool for finding bugs and enforcing code standards at editor,
commit, and CI time. [Get started.](https://semgrep.dev/docs/getting-started/)

This API is documented in the **OpenAPI format**.

### Authentication

The API supports authentication with an API token with the "Web API" permission, without limited
scopes of access.

You can provision an API token [from the Settings page](https://semgrep.dev/orgs/-/settings/tokens).

### Terms of Use

Please note, the materials made available herein are subject to the
[Semgrep Terms of Use](https://semgrep.dev/resources/website-terms/), and your
access or use of any of the same is your acknowledgment and acceptance of the
such terms.

<br>


___


## Install the Package

Run the following command from your project directory to install the package from npm:

```bash
npm install apimatic-semgrep-sdk@0.0.2
```

For additional package details, see the [Npm page for the apimatic-semgrep-sdk@0.0.2 npm](https://www.npmjs.com/package/apimatic-semgrep-sdk/v/0.0.2).

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `30000` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/partial-logging-options.md) | Logging Configuration to enable logging |
| semgrepAdminJwtCredentials | [`SemgrepAdminJwtCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/auth/oauth-2-bearer-token.md) | The credential object for semgrepAdminJwt |
| semgrepJwtCredentials | [`SemgrepJwtCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/auth/oauth-2-bearer-token-1.md) | The credential object for semgrepJwt |
| semgrepWebTokenCredentials | [`SemgrepWebTokenCredentials`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/auth/oauth-2-bearer-token-2.md) | The credential object for semgrepWebToken |

The API client can be initialized as follows:

### Code-Based Client Initialization

```ts
import { Client, Environment, LogLevel } from 'apimatic-semgrep-sdk';

const client = new Client({
  semgrepAdminJwtCredentials: {
    accessToken: 'AccessToken'
  },
  semgrepJwtCredentials: {
    accessToken: 'AccessToken'
  },
  semgrepWebTokenCredentials: {
    accessToken: 'AccessToken'
  },
  timeout: 30000,
  environment: Environment.Production,
  logging: {
    logLevel: LogLevel.Info,
    logRequest: {
      logBody: true
    },
    logResponse: {
      logHeaders: true
    }
  },
});
```

### Configuration-Based Client Initialization

```ts
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'apimatic-semgrep-sdk';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/configuration-based-client-initialization.md) section for details.

### Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'apimatic-semgrep-sdk';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`SemgrepAdminJWT (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/auth/oauth-2-bearer-token.md)
* [`SemgrepJWT (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/auth/oauth-2-bearer-token-1.md)
* [`SemgrepWebToken (OAuth 2 Bearer token)`](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/auth/oauth-2-bearer-token-2.md)

## List of APIs

* [Deployments Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/deployments-service.md)
* [Findings Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/findings-service.md)
* [Misc Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/misc-service.md)
* [Policies Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/policies-service.md)
* [Projects Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/projects-service.md)
* [Scans Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/scans-service.md)
* [Secrets Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/secrets-service.md)
* [Supply Chain Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/supply-chain-service.md)
* [Ticketing Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/ticketing-service.md)
* [Triage Service](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/controllers/triage-service.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/http-client-options.md)
* [RetryConfiguration](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/retry-configuration.md)
* [ProxySettings](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/proxy-settings.md)
* [Configuration-Based Client Initialization](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/configuration-based-client-initialization.md)
* [Environment-Based Client Initialization](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/environment-based-client-initialization.md)
* [PartialLoggingOptions](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/partial-logging-options.md)
* [PartialRequestLoggingOptions](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/partial-request-logging-options.md)
* [PartialResponseLoggingOptions](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/partial-response-logging-options.md)
* [LoggerInterface](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/logger-interface.md)

### HTTP

* [HttpRequest](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/api-response.md)
* [ApiError](https://www.github.com/sdks-io/apimatic-semgrep-js-sdk/tree/0.0.2/doc/api-error.md)

