# Function: recipientStealthPoint()

> **recipientStealthPoint**(`viewingKey`, `spendPubKey`, `ephemeralPubKey`, `solanaSpendPubKey?`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:213](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L213)

Recompute an owned output's stealth address + uncompressed public-key point from
its ephemeral public key, using the viewing PRIVATE key and the spending PUBLIC
key only — never the spending private key. This is the view-only dual of
[computeStealthAddressAndViewTag](/sdk/api/@opaquecash/opaque/functions/computeStealthAddressAndViewTag.md): use it to derive the Solana destination
(`deriveStealthSolanaAddress`) or verify the EVM address for a scanned output
without spending authority.

## Parameters

### viewingKey

`Uint8Array`

### spendPubKey

`Uint8Array`

### ephemeralPubKey

`Uint8Array`

### solanaSpendPubKey?

`Uint8Array`

## Returns

### solanaStealthPubKey?

> `optional` **solanaStealthPubKey?**: `Uint8Array`

32-byte ed25519 Solana stealth address point; present when `solanaSpendPubKey` is given.

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

### stealthPubKeyUncompressed

> **stealthPubKeyUncompressed**: `Uint8Array`

### viewTag

> **viewTag**: `number`
