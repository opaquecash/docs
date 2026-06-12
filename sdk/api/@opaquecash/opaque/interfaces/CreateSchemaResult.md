# Interface: CreateSchemaResult

Defined in: [packages/opaque/src/client.ts:381](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L381)

Result of [OpaqueClient.createSchema](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#createschema).

## Extends

- [`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md)

## Properties

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:383](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L383)

Derived `schemaId` (`0x`-hex bytes32).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:377](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L377)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md).[`txHash`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md#txhash)
