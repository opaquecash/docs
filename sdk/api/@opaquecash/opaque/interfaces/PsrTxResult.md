# Interface: PsrTxResult

Defined in: [packages/opaque/src/client.ts:338](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L338)

Result of a PSR write that only returns a transaction id.

## Extended by

- [`CreateSchemaResult`](CreateSchemaResult.md)
- [`IssueAttestationResult`](IssueAttestationResult.md)

## Properties

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:340](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L340)

EVM `0x` tx hash or Solana base58 signature.
