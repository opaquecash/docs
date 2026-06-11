# Function: buildActionScope()

> **buildActionScope**(`params`): `string`

Defined in: packages/psr-core/dist/scope.d.ts:22

Build a deterministic action scope string from chain + module + action id.

Use stable `actionId` values (proposal id, campaign id, …). **Do not** use timestamps alone in production.

## Parameters

### params

Scope components.

#### actionId

`string` \| `number` \| `bigint`

#### chainId

`number`

#### module

`string`

## Returns

`string`

Canonical `chainId:module:actionId` string.

## Example

```ts
const scope = buildActionScope({
  chainId: 11155111,
  module: "governance",
  actionId: "proposal-42",
});
```
