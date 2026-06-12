# Interface: PsrTxResult

Defined in: [packages/opaque/src/client.ts:375](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L375)

Result of a PSR write that only returns a transaction id.

## Extended by

- [`CreateSchemaResult`](/sdk/api/@opaquecash/opaque/interfaces/CreateSchemaResult.md)
- [`IssueAttestationResult`](/sdk/api/@opaquecash/opaque/interfaces/IssueAttestationResult.md)

## Properties

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:377](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L377)

EVM `0x` tx hash or Solana base58 signature.
