# Interface: CreateSchemaResult

Defined in: [packages/opaque/src/client.ts:435](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L435)

Result of [OpaqueClient.createSchema](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#createschema).

## Extends

- [`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md)

## Properties

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:437](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L437)

Derived `schemaId` (`0x`-hex bytes32).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:431](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L431)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md).[`txHash`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md#txhash)
