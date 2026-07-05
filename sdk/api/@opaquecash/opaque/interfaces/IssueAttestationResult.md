# Interface: IssueAttestationResult

Defined in: [packages/opaque/src/client.ts:441](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L441)

Result of [OpaqueClient.issueAttestation](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md#issueattestation).

## Extends

- [`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md)

## Properties

### stealthAddressHash

> **stealthAddressHash**: `string`

Defined in: [packages/opaque/src/client.ts:445](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L445)

The 32-byte `stealth_address_hash` the attestation is bound to (`0x`-hex).

***

### txHash

> **txHash**: `string`

Defined in: [packages/opaque/src/client.ts:431](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L431)

EVM `0x` tx hash or Solana base58 signature.

#### Inherited from

[`PsrTxResult`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md).[`txHash`](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md#txhash)

***

### uid

> **uid**: `string`

Defined in: [packages/opaque/src/client.ts:443](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L443)

Attestation uid (`0x`-hex bytes32).
