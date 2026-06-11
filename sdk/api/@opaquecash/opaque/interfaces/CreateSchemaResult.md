# Interface: CreateSchemaResult

Defined in: [packages/opaque/src/client.ts:344](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L344)

Result of [OpaqueClient.createSchema](../classes/OpaqueClient.md#createschema).

## Extends

- [`PsrTxResult`](PsrTxResult.md)

## Properties

### schemaId

> **schemaId**: `string`

Defined in: [packages/opaque/src/client.ts:346](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L346)

Derived `schemaId` (`0x`-hex bytes32).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:340](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L340)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](PsrTxResult.md).[`txHash`](PsrTxResult.md#txhash)
