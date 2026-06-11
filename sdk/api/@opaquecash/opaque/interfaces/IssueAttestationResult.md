# Interface: IssueAttestationResult

Defined in: [packages/opaque/src/client.ts:350](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L350)

Result of [OpaqueClient.issueAttestation](../classes/OpaqueClient.md#issueattestation).

## Extends

- [`PsrTxResult`](PsrTxResult.md)

## Properties

### stealthAddressHash

> **stealthAddressHash**: `string`

Defined in: [packages/opaque/src/client.ts:354](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L354)

The 32-byte `stealth_address_hash` the attestation is bound to (`0x`-hex).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:340](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L340)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](PsrTxResult.md).[`txHash`](PsrTxResult.md#txhash)

***

### uid

> **uid**: `string`

Defined in: [packages/opaque/src/client.ts:352](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L352)

Attestation uid (`0x`-hex bytes32).
