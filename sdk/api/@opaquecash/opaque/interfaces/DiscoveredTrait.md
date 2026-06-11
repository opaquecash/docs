# Interface: DiscoveredTrait

Defined in: packages/psr-core/dist/types.d.ts:20

Trait discovered for the connected recipient (app-level view over Attestation).

## Properties

### attestationId

> **attestationId**: `number`

Defined in: packages/psr-core/dist/types.d.ts:22

Numeric attestation id (matches circuit public input).

***

### blockNumber

> **blockNumber**: `number`

Defined in: packages/psr-core/dist/types.d.ts:27

***

### discoveredAt

> **discoveredAt**: `number`

Defined in: packages/psr-core/dist/types.d.ts:29

Unix ms when the trait was discovered client-side.

***

### ephemeralPubkey?

> `optional` **ephemeralPubkey?**: `number`[]

Defined in: packages/psr-core/dist/types.d.ts:31

Ephemeral pubkey from the announcement (compressed bytes).

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: packages/psr-core/dist/types.d.ts:24

One-time stealth address.

***

### txHash

> **txHash**: `string`

Defined in: packages/psr-core/dist/types.d.ts:26

Announcement transaction hash.
