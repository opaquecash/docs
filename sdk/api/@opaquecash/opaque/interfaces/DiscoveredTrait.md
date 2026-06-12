# Interface: DiscoveredTrait

Defined in: packages/psr-core/dist/types.d.ts:22

Trait discovered for the connected recipient (app-level view over Attestation).

## Properties

### attestationId

> **attestationId**: [`AttestationIdentifier`](/sdk/api/@opaquecash/opaque/type-aliases/AttestationIdentifier.md)

Defined in: packages/psr-core/dist/types.d.ts:24

Numeric attestation id (matches circuit public input).

***

### attestationUid?

> `optional` **attestationUid?**: `string`

Defined in: packages/psr-core/dist/types.d.ts:41

V2 attestation UID as bytes32 hex.

***

### blockNumber

> **blockNumber**: `number`

Defined in: packages/psr-core/dist/types.d.ts:29

***

### dataHex?

> `optional` **dataHex?**: `string`

Defined in: packages/psr-core/dist/types.d.ts:43

Encoded V2 attestation payload, if available.

***

### discoveredAt

> **discoveredAt**: `number`

Defined in: packages/psr-core/dist/types.d.ts:31

Unix ms when the trait was discovered client-side.

***

### ephemeralPubkey?

> `optional` **ephemeralPubkey?**: `number`[]

Defined in: packages/psr-core/dist/types.d.ts:33

Ephemeral pubkey from the announcement (compressed bytes).

***

### issuer?

> `optional` **issuer?**: `string`

Defined in: packages/psr-core/dist/types.d.ts:39

V2 issuer identity encoded as 32-byte hex.

***

### issuerAuthorized?

> `optional` **issuerAuthorized?**: `boolean`

Defined in: packages/psr-core/dist/types.d.ts:50

***

### isValid?

> `optional` **isValid?**: `boolean`

Defined in: packages/psr-core/dist/types.d.ts:49

Scanner-side validity and authorization checks.

***

### merkleLeafPreimage?

> `optional` **merkleLeafPreimage?**: [`V2MerkleLeafPreimage`](/sdk/api/@opaquecash/opaque/interfaces/V2MerkleLeafPreimage.md)

Defined in: packages/psr-core/dist/types.d.ts:47

V2 leaf preimage fields needed by the prover.

***

### nonce?

> `optional` **nonce?**: `string`

Defined in: packages/psr-core/dist/types.d.ts:45

V2 leaf nonce as bytes32 hex.

***

### schemaId?

> `optional` **schemaId?**: `string`

Defined in: packages/psr-core/dist/types.d.ts:35

V2 schema id, when discovered from a schema-bound attestation announcement.

***

### schemaName?

> `optional` **schemaName?**: `string` \| `null`

Defined in: packages/psr-core/dist/types.d.ts:37

Optional schema display name from the registry snapshot.

***

### stealthAddress

> **stealthAddress**: `string`

Defined in: packages/psr-core/dist/types.d.ts:26

One-time stealth address.

***

### txHash

> **txHash**: `string`

Defined in: packages/psr-core/dist/types.d.ts:28

Announcement transaction hash.
