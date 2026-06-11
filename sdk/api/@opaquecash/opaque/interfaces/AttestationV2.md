# Interface: AttestationV2

Defined in: packages/psr-core/dist/attestation.d.ts:19

A decoded V2 attestation record (chain-neutral view).

## Properties

### address

> **address**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:21

Stable id (== uid).

***

### createdAt

> **createdAt**: `number`

Defined in: packages/psr-core/dist/attestation.d.ts:33

Block/slot when created.

***

### dataHex

> **dataHex**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:31

Encoded attestation data as 0x-hex.

***

### expirationSlot

> **expirationSlot**: `number`

Defined in: packages/psr-core/dist/attestation.d.ts:35

0 = no expiry.

***

### issuer

> **issuer**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:27

Issuer wallet/address.

***

### refUid

> **refUid**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:39

Reference uid (zeros = none).

***

### revocationSlot

> **revocationSlot**: `number`

Defined in: packages/psr-core/dist/attestation.d.ts:37

0 = not revoked.

***

### schemaId

> **schemaId**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:25

schema id as 0x-hex.

***

### stealthAddressHash

> **stealthAddressHash**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:29

Privacy-preserving stealth-address hash (bytes32 0x-hex).

***

### uid

> **uid**: `string`

Defined in: packages/psr-core/dist/attestation.d.ts:23

uid = sha256(schema_id || issuer || stealth_address_hash || block).
