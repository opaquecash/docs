# Interface: PsrTxResult

Defined in: [packages/opaque/src/client.ts:429](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L429)

Result of a PSR write that only returns a transaction id.

## Extended by

- [`CreateSchemaResult`](/sdk/api/@opaquecash/opaque/interfaces/CreateSchemaResult.md)
- [`IssueAttestationResult`](/sdk/api/@opaquecash/opaque/interfaces/IssueAttestationResult.md)

## Properties

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:431](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L431)

EVM `0x` tx hash or Solana base58 signature.
