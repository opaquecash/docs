# Interface: CreateSchemaResult

Defined in: [packages/opaque/src/client.ts:364](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L364)

Result of [OpaqueClient.createSchema](../classes/OpaqueClient.md#createschema).

## Extends

- [`PsrTxResult`](PsrTxResult.md)

## Properties

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:366](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L366)

Derived `schemaId` (`0x`-hex bytes32).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:360](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L360)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](PsrTxResult.md).[`txHash`](PsrTxResult.md#txhash)
