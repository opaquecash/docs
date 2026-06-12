# Interface: IssueAttestationResult

Defined in: [packages/opaque/src/client.ts:387](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L387)

Result of [OpaqueClient.issueAttestation](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#issueattestation).

## Extends

- [`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md)

## Properties

### stealthAddressHash

> **stealthAddressHash**: `string`

Defined in: [packages/opaque/src/client.ts:391](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L391)

The 32-byte `stealth_address_hash` the attestation is bound to (`0x`-hex).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:377](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L377)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md).[`txHash`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md#txhash)

***

### uid

> **uid**: `string`

Defined in: [packages/opaque/src/client.ts:389](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L389)

Attestation uid (`0x`-hex bytes32).
