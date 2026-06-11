# Function: selectSigner()

> **selectSigner**\<`C`\>(`wallets`, `chain`): `Extract`\<[`EvmUnifiedSigner`](../interfaces/EvmUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `Extract`\<[`SolanaUnifiedSigner`](../interfaces/SolanaUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `undefined`

Defined in: [packages/opaque/src/signer.ts:78](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/signer.ts#L78)

Pick the first signer for a chain out of a one-or-many `wallets` argument.

## Type Parameters

### C

`C` *extends* `"ethereum"` \| `"solana"`

## Parameters

### wallets

[`UnifiedSigner`](../type-aliases/UnifiedSigner.md) \| [`UnifiedSigner`](../type-aliases/UnifiedSigner.md)[]

### chain

`C`

## Returns

`Extract`\<[`EvmUnifiedSigner`](../interfaces/EvmUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `Extract`\<[`SolanaUnifiedSigner`](../interfaces/SolanaUnifiedSigner.md), \{ `chain`: `C`; \}\> \| `undefined`
