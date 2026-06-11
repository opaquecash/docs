# Interface: UabPayload

Defined in: packages/stealth-core/dist/payload.d.ts:24

Decoded cross-chain announcement payload.

## Properties

### ephemeralPubKey

> **ephemeralPubKey**: `Uint8Array`

Defined in: packages/stealth-core/dist/payload.d.ts:28

Compressed secp256k1 ephemeral public key (33 bytes).

***

### metadata

> **metadata**: `Uint8Array`

Defined in: packages/stealth-core/dist/payload.d.ts:36

Up to 24 sender-defined bytes; the view tag is NOT repeated here.

***

### schemeId

> **schemeId**: `number`

Defined in: packages/stealth-core/dist/payload.d.ts:34

CSAP / ERC-5564 scheme id (1 = secp256k1).

***

### sourceChainId

> **sourceChainId**: `number`

Defined in: packages/stealth-core/dist/payload.d.ts:32

Wormhole chain id of the origin chain (2 = Ethereum, 1 = Solana).

***

### stealthAddress

> **stealthAddress**: `Uint8Array`

Defined in: packages/stealth-core/dist/payload.d.ts:30

32-byte stealth-address field; the low 20 bytes are the EVM-style address.

***

### viewTag

> **viewTag**: `number`

Defined in: packages/stealth-core/dist/payload.d.ts:26

EIP-5564 view tag (the metadata's first byte).
