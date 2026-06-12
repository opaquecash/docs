# Function: selectSigner()

> **selectSigner**\<`C`\>(`wallets`, `chain`): `Extract`\<[`EvmUnifiedSigner`](/sdk/api/@opaquecash/opaque/interfaces/EvmUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `Extract`\<[`SolanaUnifiedSigner`](/sdk/api/@opaquecash/opaque/interfaces/SolanaUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `undefined`

Defined in: [packages/opaque/src/signer.ts:78](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/signer.ts#L78)

Pick the first signer for a chain out of a one-or-many `wallets` argument.

## Type Parameters

### C

`C` *extends* `"ethereum"` \| `"solana"`

## Parameters

### wallets

[`UnifiedSigner`](/sdk/api/@opaquecash/opaque/type-aliases/UnifiedSigner.md) \| [`UnifiedSigner`](/sdk/api/@opaquecash/opaque/type-aliases/UnifiedSigner.md)[]

### chain

`C`

## Returns

`Extract`\<[`EvmUnifiedSigner`](/sdk/api/@opaquecash/opaque/interfaces/EvmUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `Extract`\<[`SolanaUnifiedSigner`](/sdk/api/@opaquecash/opaque/interfaces/SolanaUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `undefined`
