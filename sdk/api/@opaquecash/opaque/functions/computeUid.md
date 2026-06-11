# Function: computeUid()

> **computeUid**(`schemaId`, `issuer`, `stealthAddressHash`, `blockNumber`): `` `0x${string}` ``

Defined in: packages/psr-core/dist/attestation.d.ts:45

`uid = sha256(abi.encodePacked(schemaId, issuer, stealthAddressHash, blockNumber))`,
matching the attestation engine's `computeUid` on-chain.

## Parameters

### schemaId

`` `0x${string}` ``

### issuer

`` `0x${string}` ``

### stealthAddressHash

`` `0x${string}` ``

### blockNumber

`bigint`

## Returns

`` `0x${string}` ``
