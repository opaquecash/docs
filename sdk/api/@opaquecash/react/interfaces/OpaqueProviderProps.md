# Interface: OpaqueProviderProps

Defined in: [context.ts:7](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/context.ts#L7)

Props for [OpaqueProvider](/sdk/api/@opaquecash/react/functions/OpaqueProvider.md).

## Properties

### children?

> `optional` **children?**: `ReactNode`

Defined in: [context.ts:10](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/context.ts#L10)

***

### client

> **client**: [`OpaqueClient`](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md) \| `null`

Defined in: [context.ts:9](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/react/src/context.ts#L9)

The shared client, or `null` while the wallet/session is not connected yet.
