# Interface: PrepareStealthSendResult

Defined in: [packages/opaque/src/client.ts:464](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L464)

Result of preparing a stealth send (ephemeral material + announce fields).

## Properties

### ephemeralPrivateKey

> **ephemeralPrivateKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:471](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L471)

32-byte ephemeral private key — store securely if you need ghost / later announce.

***

### ephemeralPublicKey

> **ephemeralPublicKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:469](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L469)

33-byte compressed ephemeral public key.

***

### metadata

> **metadata**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:473](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L473)

Metadata bytes for `announce` (view tag byte; extend with WASM for PSR).

***

### schemeId

> **schemeId**: `bigint`

Defined in: [packages/opaque/src/client.ts:465](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L465)

***

### stealthAddress

> **stealthAddress**: `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:466](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L466)

***

### stealthPubKey

> **stealthPubKey**: `Uint8Array`

Defined in: [packages/opaque/src/client.ts:478](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L478)

Uncompressed (65-byte) stealth public-key point. Needed to derive the Solana destination
account (`deriveStealthSolanaAddress`); not required for the EVM `announce`.

***

### viewTag

> **viewTag**: `number`

Defined in: [packages/opaque/src/client.ts:467](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L467)
