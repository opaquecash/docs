# Interface: IssueAttestationResult

Defined in: [packages/opaque/src/client.ts:321](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L321)

Result of [OpaqueClient.issueAttestation](../classes/OpaqueClient.md#issueattestation).

## Extends

- [`PsrTxResult`](PsrTxResult.md)

## Properties

### stealthAddressHash

> **stealthAddressHash**: `string`

Defined in: [packages/opaque/src/client.ts:325](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L325)

The 32-byte `stealth_address_hash` the attestation is bound to (`0x`-hex).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:311](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L311)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](PsrTxResult.md).[`txHash`](PsrTxResult.md#txhash)

***

### uid

> **uid**: `string`

Defined in: [packages/opaque/src/client.ts:323](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L323)

Attestation uid (`0x`-hex bytes32).
