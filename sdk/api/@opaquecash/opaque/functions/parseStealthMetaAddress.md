# Function: parseStealthMetaAddress()

> **parseStealthMetaAddress**(`metaHex`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:116](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L116)

## Parameters

### metaHex

`` `0x${string}` ``

## Returns

### solanaSpendPubKey?

> `optional` **solanaSpendPubKey?**: `Uint8Array`

ed25519 Solana spend public key `S_ed`; present only for a 98-byte meta-address.

### spendPubKey

> **spendPubKey**: `Uint8Array`

### viewPubKey

> **viewPubKey**: `Uint8Array`
