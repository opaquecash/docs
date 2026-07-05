# Function: viewOnlyMetaAddress()

> **viewOnlyMetaAddress**(`viewingKey`, `spendPubKey`, `solanaSpendPubKey?`): `object`

Defined in: [packages/opaque/src/crypto/dksap.ts:79](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L79)

Build the meta-address for view-only delegation (CSAP §2.8): the scanner holds the viewing
PRIVATE key `v` and the spending PUBLIC key `S` (plus the ed25519 Solana spend PUBLIC key `S_ed`
for Solana scanning), never any spending private key. The viewing public key `V = v·G` is derived
here; the result `V‖S[‖S_ed]` matches [keysToStealthMetaAddress](/sdk/api/@opaquecash/opaque/functions/keysToStealthMetaAddress.md). Omit `solanaSpendPubKey`
for an Ethereum-only (66-byte) delegation.

## Parameters

### viewingKey

`Uint8Array`

### spendPubKey

`Uint8Array`

### solanaSpendPubKey?

`Uint8Array`

## Returns

`object`

### metaAddress

> **metaAddress**: `Uint8Array`

### S

> **S**: `Uint8Array`

### solanaSpendPubKey?

> `optional` **solanaSpendPubKey?**: `Uint8Array`

### V

> **V**: `Uint8Array`
