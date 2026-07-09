
# List Dependencies Response

*This model accepts additional fields of type unknown.*

## Structure

`ListDependenciesResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cursor` | `string \| undefined` | Optional | Pass to next request to get next page of results. |
| `dependencies` | [`ProtosScaV1FoundDependency[]`](../../doc/models/protos-sca-v1-found-dependency.md) | Required | List of dependencies. |
| `hasMore` | `boolean` | Required | True if there are more dependencies to get. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Ecosystem1, ListDependenciesResponse } from 'apimatic-semgrep-sdk';

const listDependenciesResponse: ListDependenciesResponse = {
  dependencies: [
    {
      definedAt: {
        committedAt: '2016-03-13T12:52:32.123Z',
        endCol: 'endCol8',
        endLine: 'endLine2',
        path: 'path2',
        startCol: 'startCol2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      ecosystem: Ecosystem1.Cocoapods,
      licenses: [
        'licenses3',
        'licenses4',
        'licenses5'
      ],
      manifestDefinition: {
        committedAt: '2016-03-13T12:52:32.123Z',
        endCol: 'endCol0',
        endLine: 'endLine4',
        path: 'path4',
        startCol: 'startCol4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      mPackage: {
        name: 'name8',
        versionSpecifier: 'versionSpecifier6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'id': '1',
        'name': 'dependency1',
        'version': '1.0.0'
      },
    },
    {
      definedAt: {
        committedAt: '2016-03-13T12:52:32.123Z',
        endCol: 'endCol8',
        endLine: 'endLine2',
        path: 'path2',
        startCol: 'startCol2',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      ecosystem: Ecosystem1.Cocoapods,
      licenses: [
        'licenses3',
        'licenses4',
        'licenses5'
      ],
      manifestDefinition: {
        committedAt: '2016-03-13T12:52:32.123Z',
        endCol: 'endCol0',
        endLine: 'endLine4',
        path: 'path4',
        startCol: 'startCol4',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      mPackage: {
        name: 'name8',
        versionSpecifier: 'versionSpecifier6',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'id': '2',
        'name': 'dependency2',
        'version': '2.0.0'
      },
    }
  ],
  hasMore: false,
  cursor: 'cursor2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

