# Interface: IssueAttestationResult

Defined in: [packages/opaque/src/client.ts:370](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L370)

Result of [OpaqueClient.issueAttestation](../classes/OpaqueClient.md#issueattestation).

## Extends

- [`PsrTxResult`](PsrTxResult.md)

## Properties

### stealthAddressHash

> **stealthAddressHash**: `string`

Defined in: [packages/opaque/src/client.ts:374](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L374)

The 32-byte `stealth_address_hash` the attestation is bound to (`0x`-hex).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:360](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L360)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](PsrTxResult.md).[`txHash`](PsrTxResult.md#txhash)

***

### uid

> **uid**: `string`

Defined in: [packages/opaque/src/client.ts:372](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L372)

Attestation uid (`0x`-hex bytes32).
