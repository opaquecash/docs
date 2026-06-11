# Interface: CreateSchemaResult

Defined in: [packages/opaque/src/client.ts:315](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L315)

Result of [OpaqueClient.createSchema](../classes/OpaqueClient.md#createschema).

## Extends

- [`PsrTxResult`](PsrTxResult.md)

## Properties

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:317](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L317)

Derived `schemaId` (`0x`-hex bytes32).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:311](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L311)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](PsrTxResult.md).[`txHash`](PsrTxResult.md#txhash)
