# Interface: PsrTxResult

Defined in: [packages/opaque/src/client.ts:309](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L309)

Result of a PSR write that only returns a transaction id.

## Extended by

- [`CreateSchemaResult`](CreateSchemaResult.md)
- [`IssueAttestationResult`](IssueAttestationResult.md)

## Properties

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:311](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L311)

EVM `0x` tx hash or Solana base58 signature.
