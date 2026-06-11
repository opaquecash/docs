# Function: requestSetupSignature()

> **requestSetupSignature**(`signer`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/signer.ts:43](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/signer.ts#L43)

Prompt `signer` for the canonical [SETUP\_MESSAGE](../variables/SETUP_MESSAGE.md) signature used as HKDF
entropy for the viewing/spending keys. Ethereum signs via `personal_sign`
(WalletClient when given, raw EIP-1193 otherwise); Solana signs the UTF-8 bytes
via wallet-adapter `signMessage`. The signature never goes on-chain.

## Parameters

### signer

[`UnifiedSigner`](../type-aliases/UnifiedSigner.md)

## Returns

`Promise`\<`` `0x${string}` ``\>
