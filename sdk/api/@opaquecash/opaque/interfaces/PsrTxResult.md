# Interface: PsrTxResult

Defined in: [packages/opaque/src/client.ts:358](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L358)

Result of a PSR write that only returns a transaction id.

## Extended by

- [`CreateSchemaResult`](CreateSchemaResult.md)
- [`IssueAttestationResult`](IssueAttestationResult.md)

## Properties

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:360](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L360)

EVM `0x` tx hash or Solana base58 signature.
