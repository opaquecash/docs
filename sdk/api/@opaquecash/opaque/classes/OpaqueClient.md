# Class: OpaqueClient

Defined in: [packages/opaque/src/client.ts:555](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L555)

## Properties

### buildReputationActionScope

> `static` **buildReputationActionScope**: (`params`) => `string` = `buildActionScope`

Defined in: [packages/opaque/src/client.ts:2373](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2373)

Deterministic scope string for reputation actions (`chainId:module:actionId`).
Same as [buildActionScope](../functions/buildActionScope.md) in `@opaquecash/psr-core`.

Build a deterministic action scope string from chain + module + action id.

Use stable `actionId` values (proposal id, campaign id, …). **Do not** use timestamps alone in production.

#### Parameters

##### params

Scope components.

###### actionId

`string` \| `number` \| `bigint`

###### chainId

`number`

###### module

`string`

#### Returns

`string`

Canonical `chainId:module:actionId` string.

#### Example

```ts
const scope = buildActionScope({
  chainId: 11155111,
  module: "governance",
  actionId: "proposal-42",
});
```

***

### reputationExternalNullifierFromScope

> `static` **reputationExternalNullifierFromScope**: (`scope`) => `bigint` = `externalNullifierFromScope`

Defined in: [packages/opaque/src/client.ts:2379](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2379)

Map a scope string to the circuit `externalNullifier` scalar (keccak, uint256).
Same as [externalNullifierFromScope](../functions/externalNullifierFromScope.md) in `@opaquecash/psr-core`.

Map a scope string to a `uint256` external nullifier using Keccak-256 (left-padded to 32 bytes).

Must stay consistent with how your circuit expects the external nullifier input.

#### Parameters

##### scope

`string`

Output of [buildActionScope](../functions/buildActionScope.md).

#### Returns

`bigint`

## Methods

### addSchemaDelegate()

> **addSchemaDelegate**(`chain`, `schemaId`, `delegate`): `Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

Defined in: [packages/opaque/src/client.ts:1878](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1878)

Authority-only: authorize `delegate` to issue under `schemaId`.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### schemaId

`string`

##### delegate

`string`

#### Returns

`Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

***

### announcementsJsonForReputationWitness()

> **announcementsJsonForReputationWitness**(`rows`): `string`

Defined in: [packages/opaque/src/client.ts:2212](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2212)

JSON array string in the Rust scanner's announcement format (general scanner interop;
no longer consumed by [generateReputationProof](#generatereputationproof), which builds V2 witnesses directly).

#### Parameters

##### rows

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]

#### Returns

`string`

***

### buildAnnounceTransactionRequest()

> **buildAnnounceTransactionRequest**(`send`): [`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)

Defined in: [packages/opaque/src/client.ts:1251](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1251)

Build calldata for `announce` so the developer can prompt the user to broadcast.

#### Parameters

##### send

[`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

#### Returns

[`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)

***

### buildAnnounceTransactionRequestForGhost()

> **buildAnnounceTransactionRequestForGhost**(`ephemeralPrivateKey`): [`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)

Defined in: [packages/opaque/src/client.ts:1230](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1230)

Build `announce` calldata after you only have the stored 32-byte ephemeral secret from
[prepareGhostReceive](#prepareghostreceive) (or any prior [prepareStealthSend](#preparestealthsend) to your meta-address).
Recomputes stealth address and pubkey material deterministically. If you still have the full
[PrepareStealthSendResult](../interfaces/PrepareStealthSendResult.md) object, [buildAnnounceTransactionRequest](#buildannouncetransactionrequest) is enough.

#### Parameters

##### ephemeralPrivateKey

`Uint8Array`

#### Returns

[`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)

***

### buildAnnounceWithRelay()

> **buildAnnounceWithRelay**(`chain`, `send`, `opts?`): `Promise`\<[`AnnounceWithRelayResult`](../type-aliases/AnnounceWithRelayResult.md)\>

Defined in: [packages/opaque/src/client.ts:1329](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1329)

Build a CROSS-CHAIN announce for either chain, dispatching on `chain`. Emits the local
announcement AND relays the 96-byte payload over Wormhole. Ethereum returns a `{to,data,value}`
request (`value` is the Wormhole fee); Solana returns `instructions` + extra `signers` (the
fresh Wormhole message keypair) — both must co-sign with the wallet. Pass the same
[PrepareStealthSendResult](../interfaces/PrepareStealthSendResult.md) you'd use for a native announce.

EVM honours `consistencyLevel`; Solana honours `batchId` (Wormhole nonce) and `wormholeFee`
(auto-fetched from the core bridge when omitted; 0 on devnet).

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### send

[`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

##### opts?

###### batchId?

`number`

###### consistencyLevel?

`number`

###### wormholeFee?

`bigint`

#### Returns

`Promise`\<[`AnnounceWithRelayResult`](../type-aliases/AnnounceWithRelayResult.md)\>

***

### buildAnnounceWithRelayRequest()

> **buildAnnounceWithRelayRequest**(`send`, `opts?`): `Promise`\<[`AnnounceWithRelayRequest`](../interfaces/AnnounceWithRelayRequest.md) & `object`\>

Defined in: [packages/opaque/src/client.ts:1302](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1302)

Build a `{to,data,value}` request for a CROSS-CHAIN announce (`announceWithRelay`): it emits the
local announcement AND publishes the 96-byte payload through Wormhole. `value` is the Wormhole
message fee. Pass the same [PrepareStealthSendResult](../interfaces/PrepareStealthSendResult.md) you'd use for a native announce.

#### Parameters

##### send

[`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

##### opts?

###### consistencyLevel?

`number`

#### Returns

`Promise`\<[`AnnounceWithRelayRequest`](../interfaces/AnnounceWithRelayRequest.md) & `object`\>

***

### buildAssignReputationTransaction()

> **buildAssignReputationTransaction**(`recipientMetaAddressHex`, `attestationId`): [`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)

Defined in: [packages/opaque/src/client.ts:1775](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1775)

Issuer flow: calldata for `StealthAddressAnnouncer.announce` with PSR metadata (no asset transfer).

#### Parameters

##### recipientMetaAddressHex

`` `0x${string}` ``

##### attestationId

`bigint`

#### Returns

[`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)

***

### buildDummyAnnouncementTransactions()

> **buildDummyAnnouncementTransactions**(`n`): [`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)[]

Defined in: [packages/opaque/src/client.ts:1208](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1208)

Convenience over [generateDummyAnnouncements](#generatedummyannouncements): `n` ready-to-submit `announce`
calldata requests for this chain's announcer. Broadcast them from any account —
announcements carry no value and any caller may announce.

#### Parameters

##### n

`number`

#### Returns

[`AnnounceTransactionRequest`](../interfaces/AnnounceTransactionRequest.md)[]

***

### buildRegisterMetaAddressTransaction()

> **buildRegisterMetaAddressTransaction**(): [`RegisterMetaAddressTransactionRequest`](../interfaces/RegisterMetaAddressTransactionRequest.md)

Defined in: [packages/opaque/src/client.ts:927](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L927)

Encode `registerKeys` for the user's meta-address (they submit with `ethereumAddress`).

#### Returns

[`RegisterMetaAddressTransactionRequest`](../interfaces/RegisterMetaAddressTransactionRequest.md)

***

### createSchema()

> **createSchema**(`chain`, `params`): `Promise`\<[`CreateSchemaResult`](../interfaces/CreateSchemaResult.md)\>

Defined in: [packages/opaque/src/client.ts:1797](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1797)

Register a new schema (attestation class + issuance rules). Returns the tx id and derived
`schemaId`. `fieldDefinitions` accepts an ABI string or [FieldDef](../interfaces/FieldDef.md)s.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### params

[`CreateSchemaParams`](../interfaces/CreateSchemaParams.md)

#### Returns

`Promise`\<[`CreateSchemaResult`](../interfaces/CreateSchemaResult.md)\>

***

### deprecateSchema()

> **deprecateSchema**(`chain`, `schemaId`): `Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

Defined in: [packages/opaque/src/client.ts:1857](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1857)

Authority-only, irreversible: deprecate a schema (blocks new attestations).

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### schemaId

`string`

#### Returns

`Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

***

### discoverTraits()

> **discoverTraits**(`rows`): `Promise`\<[`DiscoveredTrait`](../interfaces/DiscoveredTrait.md)[]\>

Defined in: [packages/opaque/src/client.ts:1723](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1723)

PSR: map owned attestation markers to [DiscoveredTrait](../interfaces/DiscoveredTrait.md) list.

#### Parameters

##### rows

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]

#### Returns

`Promise`\<[`DiscoveredTrait`](../interfaces/DiscoveredTrait.md)[]\>

***

### encodeReputationMetadata()

> **encodeReputationMetadata**(`viewTag`, `attestationId`): `Uint8Array`

Defined in: [packages/opaque/src/client.ts:1751](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1751)

Encode `announce` metadata for a PSR attestation (view tag byte + `0xA7` + u64 `attestationId`).
Canonical encoding matches WASM/Rust; use with [prepareReputationAssignment](#preparereputationassignment).

#### Parameters

##### viewTag

`number`

##### attestationId

`bigint`

#### Returns

`Uint8Array`

***

### fetchAnnouncementRows()

> **fetchAnnouncementRows**(`chain`, `opts?`): `Promise`\<[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]\>

Defined in: [packages/opaque/src/client.ts:1527](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1527)

Fetch ALL native announcements on `chain` as indexer-shaped rows — unfiltered, with their
full on-chain `metadata`. This is the raw input for the metadata-aware scanners:
[discoverTraits](#discovertraits) / [getReputationTraitsFromAnnouncements](#getreputationtraitsfromannouncements) (PSR attestation
markers) and [filterOwnedAnnouncements](#filterownedannouncements). Unlike [scan](#scan), nothing is dropped, so
callers can decode announcement metadata that ownership filtering would discard.

Note: cross-chain (UAB) announcements are NOT included — the 96-byte Wormhole payload only
carries a 24-byte metadata tail, which cannot hold the 130-byte V2 attestation metadata.
For trait discovery, fetch rows natively on each chain instead.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### opts?

###### fromBlock?

`bigint`

Lower-bound cursor: EVM block number (Solana scans the most recent signatures).

###### solanaLimit?

`number`

Max Solana signatures to scan (adapter default when omitted).

###### toBlock?

`bigint`

Upper-bound EVM block; omit for the chain tip.

#### Returns

`Promise`\<[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]\>

***

### fetchCrossChainAnnouncements()

> **fetchCrossChainAnnouncements**(`opts?`): `Promise`\<[`UabIndexerAnnouncement`](../interfaces/UabIndexerAnnouncement.md)[]\>

Defined in: [packages/opaque/src/client.ts:1369](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1369)

Read inbound CROSS-CHAIN announcements (from the UABReceiver) as indexer-shaped rows, ready to
pass into [filterOwnedAnnouncements](#filterownedannouncements) alongside native rows.

#### Parameters

##### opts?

###### fromBlock?

`bigint`

###### toBlock?

`bigint` \| `"latest"`

#### Returns

`Promise`\<[`UabIndexerAnnouncement`](../interfaces/UabIndexerAnnouncement.md)[]\>

***

### fetchLatestValidReputationRoot()

> **fetchLatestValidReputationRoot**(): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/client.ts:2263](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2263)

Latest non-expired Merkle root from `OpaqueReputationVerifier.rootHistory`.

#### Returns

`Promise`\<`` `0x${string}` ``\>

***

### fetchReputationRootHistory()

> **fetchReputationRootHistory**(): `Promise`\<`object`[]\>

Defined in: [packages/opaque/src/client.ts:2280](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2280)

Full root history with per-entry validity (newest index last).

#### Returns

`Promise`\<`object`[]\>

***

### filterOwnedAnnouncements()

> **filterOwnedAnnouncements**(`rows`): `Promise`\<[`OwnedStealthOutput`](../interfaces/OwnedStealthOutput.md)[]\>

Defined in: [packages/opaque/src/client.ts:1392](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1392)

Filter indexer announcements down to outputs owned by this user (WASM scan).

#### Parameters

##### rows

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]

#### Returns

`Promise`\<[`OwnedStealthOutput`](../interfaces/OwnedStealthOutput.md)[]\>

***

### generateDummyAnnouncements()

> **generateDummyAnnouncements**(`n`): [`DummyAnnouncement`](../type-aliases/DummyAnnouncement.md)[]

Defined in: [packages/opaque/src/client.ts:1193](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1193)

Anonymity-set utility (guide §17): mint `n` decoy announcements. Each one is a fully
valid DKSAP announcement to a freshly generated THROWAWAY meta-address whose private
keys are discarded — on-chain it is indistinguishable from a real payment
announcement (valid curve points, correctly derived view tag), but nobody will ever
match or spend it. Submit them (e.g. via [buildDummyAnnouncementTransactions](#builddummyannouncementtransactions))
interleaved with real sends to grow every recipient's anonymity set.

#### Parameters

##### n

`number`

#### Returns

[`DummyAnnouncement`](../type-aliases/DummyAnnouncement.md)[]

***

### generateReputationProof()

> **generateReputationProof**(`params`): `Promise`\<[`ProofData`](../interfaces/ProofData.md)\>

Defined in: [packages/opaque/src/client.ts:2239](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2239)

V2 Groth16 proof bundle for the reputation verifiers (requires `snarkjs`).
When `artifacts` is omitted, the V2 wasm/zkey are loaded from the default hosted paths on
opaque.cash (same as the Opaque frontend `/circuits/v2/...` assets).

Public signals: `[merkle_root, attestation_id, external_nullifier, nullifier_hash]`;
`ProofData.nullifier` carries `nullifier_hash`.

#### Parameters

##### params

###### artifacts?

[`ArtifactPaths`](../interfaces/ArtifactPaths.md)

###### externalNullifier

`string`

###### issuerPkX?

`string` \| `bigint`

###### nonce?

`string` \| `bigint`

###### onProgress?

[`ProofProgressCallback`](../type-aliases/ProofProgressCallback.md)

###### stealthPrivKeyBytes

`Uint8Array`

###### trait

[`DiscoveredTrait`](../interfaces/DiscoveredTrait.md)

###### traitDataHash?

`string` \| `bigint`

#### Returns

`Promise`\<[`ProofData`](../interfaces/ProofData.md)\>

***

### getBalancesForOutputs()

> **getBalancesForOutputs**(`outputs`): `Promise`\<[`OutputBalance`](../interfaces/OutputBalance.md)[]\>

Defined in: [packages/opaque/src/client.ts:1688](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1688)

Native balance per owned stealth output across chains. Ethereum reads the stealth address
directly; Solana reconstructs the one-time key (WASM), derives the Solana stealth account, and
reads its lamports. Pass the [UnifiedOwnedOutput](../interfaces/UnifiedOwnedOutput.md)s from [scan](#scan). SPL/ERC-20 token
sums for the EVM tracked-token set live in [getBalancesFromAnnouncements](#getbalancesfromannouncements).

#### Parameters

##### outputs

[`UnifiedOwnedOutput`](../interfaces/UnifiedOwnedOutput.md)[]

#### Returns

`Promise`\<[`OutputBalance`](../interfaces/OutputBalance.md)[]\>

***

### getBalancesFromAnnouncements()

> **getBalancesFromAnnouncements**(`rows`): `Promise`\<[`TokenBalanceSummary`](../interfaces/TokenBalanceSummary.md)[]\>

Defined in: [packages/opaque/src/client.ts:1645](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1645)

Owned outputs + balances summed per tracked token (uses `rpcUrl` from config).

#### Parameters

##### rows

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]

#### Returns

`Promise`\<[`TokenBalanceSummary`](../interfaces/TokenBalanceSummary.md)[]\>

***

### getChainId()

> **getChainId**(): `number`

Defined in: [packages/opaque/src/client.ts:692](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L692)

Chain id from configuration.

#### Returns

`number`

***

### getContracts()

> **getContracts**(): `object`

Defined in: [packages/opaque/src/client.ts:707](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L707)

Resolved contract addresses for the active chain.

#### Returns

`object`

##### opaqueReputationVerifier?

> `optional` **opaqueReputationVerifier?**: `` `0x${string}` ``

##### stealthAddressAnnouncer

> **stealthAddressAnnouncer**: `` `0x${string}` ``

##### stealthMetaAddressRegistry

> **stealthMetaAddressRegistry**: `` `0x${string}` ``

***

### getEthereumAddress()

> **getEthereumAddress**(): `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:697](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L697)

Connected Ethereum address (from config).

#### Returns

`` `0x${string}` ``

***

### getMetaAddressHex()

> **getMetaAddressHex**(): `` `0x${string}` ``

Defined in: [packages/opaque/src/client.ts:702](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L702)

66-byte meta-address hex for registry / sharing.

#### Returns

`` `0x${string}` ``

***

### getMyIssuedAttestations()

> **getMyIssuedAttestations**(`chain`): `Promise`\<[`AttestationV2`](../interfaces/AttestationV2.md)[]\>

Defined in: [packages/opaque/src/client.ts:1922](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1922)

Attestations issued by this client's wallet.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

#### Returns

`Promise`\<[`AttestationV2`](../interfaces/AttestationV2.md)[]\>

***

### getMySchemas()

> **getMySchemas**(`chain`): `Promise`\<[`SchemaV2`](../interfaces/SchemaV2.md)[]\>

Defined in: [packages/opaque/src/client.ts:1835](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1835)

Schemas where this client's wallet is the authority OR an authorized delegate.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

#### Returns

`Promise`\<[`SchemaV2`](../interfaces/SchemaV2.md)[]\>

***

### getReputationTraitsFromAnnouncements()

> **getReputationTraitsFromAnnouncements**(`rows`): `Promise`\<[`DiscoveredTrait`](../interfaces/DiscoveredTrait.md)[]\>

Defined in: [packages/opaque/src/client.ts:1741](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1741)

PSR: same as [discoverTraits](#discovertraits) — alias for reputation-focused call sites.

#### Parameters

##### rows

[`IndexerAnnouncement`](../interfaces/IndexerAnnouncement.md)[]

#### Returns

`Promise`\<[`DiscoveredTrait`](../interfaces/DiscoveredTrait.md)[]\>

***

### getStealthSignerPrivateKey()

> **getStealthSignerPrivateKey**(`output`): `Uint8Array`

Defined in: [packages/opaque/src/client.ts:1607](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1607)

Reconstruct the 32-byte secp256k1 private key that controls `output`’s one-time stealth address.
Uses the same WASM path as the on-chain scanner (`reconstruct_signing_key_wasm`).

You supply gas, nonce, and broadcast: build a viem `PrivateKeyAccount` (or ethers wallet) from
the returned bytes and sign a transfer **from** `output.stealthAddress`. Never log or persist
the result beyond what your threat model allows.

#### Parameters

##### output

`Pick`\<[`OwnedStealthOutput`](../interfaces/OwnedStealthOutput.md), `"ephemeralPublicKey"`\>

#### Returns

`Uint8Array`

***

### getStealthSignerPrivateKeyForReputationTrait()

> **getStealthSignerPrivateKeyForReputationTrait**(`trait`): `Uint8Array`

Defined in: [packages/opaque/src/client.ts:2219](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2219)

One-time stealth signing key for a [DiscoveredTrait](../interfaces/DiscoveredTrait.md) (requires `ephemeralPubkey` from the scan).

#### Parameters

##### trait

[`DiscoveredTrait`](../interfaces/DiscoveredTrait.md)

#### Returns

`Uint8Array`

***

### getStealthSignerPrivateKeyFromEphemeralPrivateKey()

> **getStealthSignerPrivateKeyFromEphemeralPrivateKey**(`ephemeralPrivateKey`): `Uint8Array`

Defined in: [packages/opaque/src/client.ts:1629](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1629)

Same as [getStealthSignerPrivateKey](#getstealthsignerprivatekey) when you only have the 32-byte ephemeral **private**
key from [prepareGhostReceive](#prepareghostreceive) / [prepareStealthSend](#preparestealthsend) (e.g. ghost storage) instead
of an indexer row with `ephemeralPublicKey`.

#### Parameters

##### ephemeralPrivateKey

`Uint8Array`

#### Returns

`Uint8Array`

***

### isMetaAddressRegistered()

> **isMetaAddressRegistered**(`chain`): `Promise`\<`boolean`\>

Defined in: [packages/opaque/src/client.ts:980](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L980)

Whether THIS wallet's meta-address is already registered on `chain` (Ethereum reads its
configured `ethereumAddress`; Solana reads the `solanaWallet` pubkey).

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

#### Returns

`Promise`\<`boolean`\>

***

### isReputationRootValid()

> **isReputationRootValid**(`root`): `Promise`\<`boolean`\>

Defined in: [packages/opaque/src/client.ts:2271](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2271)

Whether the verifier currently accepts this root (exists and not past expiry).

#### Parameters

##### root

`` `0x${string}` ``

#### Returns

`Promise`\<`boolean`\>

***

### issueAttestation()

> **issueAttestation**(`chain`, `params`): `Promise`\<[`IssueAttestationResult`](../interfaces/IssueAttestationResult.md)\>

Defined in: [packages/opaque/src/client.ts:1946](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1946)

Issue a schema-bound attestation against a stealth identity. Resolves the recipient to a
`stealth_address_hash`, encodes the field values per the schema, submits `attest`, and
(when the recipient is a meta-address and `announce` is not `false`) publishes a discovery
announcement so the recipient's scanner can find the trait. Verifies the wallet is an
authorized issuer first.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### params

[`IssueAttestationParams`](../interfaces/IssueAttestationParams.md)

#### Returns

`Promise`\<[`IssueAttestationResult`](../interfaces/IssueAttestationResult.md)\>

***

### prepareGhostReceive()

> **prepareGhostReceive**(): [`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

Defined in: [packages/opaque/src/client.ts:1220](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1220)

Manual “ghost” receive: derive a one-time stealth address for **this** wallet’s meta-address
without any on-chain announcement yet. Cryptographically this is [prepareStealthSend](#preparestealthsend)
with [getMetaAddressHex](#getmetaaddresshex); you must persist `ephemeralPrivateKey` (and optionally the
full prep) securely to sweep funds or to announce later.

#### Returns

[`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

***

### prepareReputationAssignment()

> **prepareReputationAssignment**(`recipientMetaAddressHex`, `attestationId`): [`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

Defined in: [packages/opaque/src/client.ts:1763](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1763)

Issuer flow: derive one-time stealth material for the recipient and embed `attestationId` in metadata.

#### Parameters

##### recipientMetaAddressHex

`` `0x${string}` ``

##### attestationId

`bigint`

#### Returns

[`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

***

### prepareStealthSend()

> **prepareStealthSend**(`recipientMetaAddressHex`): [`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

Defined in: [packages/opaque/src/client.ts:995](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L995)

Derive a one-time stealth address for sending to a recipient meta-address.

#### Parameters

##### recipientMetaAddressHex

`` `0x${string}` ``

#### Returns

[`PrepareStealthSendResult`](../interfaces/PrepareStealthSendResult.md)

***

### registerMetaAddress()

> **registerMetaAddress**(`chain`): `Promise`\<[`RegisterMetaAddressResult`](../interfaces/RegisterMetaAddressResult.md)\>

Defined in: [packages/opaque/src/client.ts:949](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L949)

Register THIS wallet's 66-byte meta-address on-chain so others can resolve it, dispatching on
`chain`. Submits the transaction with the configured signer (`ethereumWalletClient` /
`ethereumProvider` for Ethereum, `solanaWallet` for Solana) and returns the tx id. For a
calldata-only request you submit yourself, see [buildRegisterMetaAddressTransaction](#buildregistermetaaddresstransaction)
(Ethereum) or `SolanaAdapter.buildRegisterKeysInstruction`.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

#### Returns

`Promise`\<[`RegisterMetaAddressResult`](../interfaces/RegisterMetaAddressResult.md)\>

***

### removeSchemaDelegate()

> **removeSchemaDelegate**(`chain`, `schemaId`, `delegate`): `Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

Defined in: [packages/opaque/src/client.ts:1900](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1900)

Authority-only: revoke a delegate's issuance rights under `schemaId`.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### schemaId

`string`

##### delegate

`string`

#### Returns

`Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

***

### resolveOpaqueMetaAddress()

> **resolveOpaqueMetaAddress**(`name`): `Promise`\<`` `0x${string}` ``\>

Defined in: [packages/opaque/src/client.ts:834](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L834)

Resolve an Opaque Name Service name (`alice.opq.eth`; `alice.opqtest.eth` on
testnet) to its meta-address (spec/ONS.md §7). Tries the Solana mirror PDA first
(one account read, no Ethereum RPC — needs [OpaqueClientConfig.solana](../interfaces/OpaqueClientConfig.md#solana));
falls back to the canonical OpaqueNameRegistry (ENSIP-10) over the scan RPC.
Both paths point-validate the 33-byte halves. Mirror records lag the canonical
record by Wormhole latency (eventually consistent, canonical-chain-wins).

#### Parameters

##### name

`string`

#### Returns

`Promise`\<`` `0x${string}` ``\>

***

### resolveRecipient()

> **resolveRecipient**(`input`): `Promise`\<[`ResolvedRecipient`](../interfaces/ResolvedRecipient.md)\>

Defined in: [packages/opaque/src/client.ts:768](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L768)

Resolve ANY supported recipient identity to its 66-byte meta-address (CSAP §2.9):

| Input | Path |
|-------|------|
| 66-byte meta-address (optionally `st:opq:`-prefixed) | validated and passed through |
| `0x…` 20-byte EVM address | ERC-6538 `StealthMetaAddressRegistry` |
| Solana base58 pubkey | `stealth-registry` PDA (needs [OpaqueClientConfig.solana](../interfaces/OpaqueClientConfig.md#solana)) |
| `ipfs://…` / bare CID | DID document fetch via gateways (configure [OpaqueClientConfig.ipfs](../interfaces/OpaqueClientConfig.md#ipfs)) |
| ONS name (`alice.opq.eth`) | Solana mirror PDA first, canonical OpaqueNameRegistry fallback (spec/ONS.md) |
| other `*.eth` | ENS `com.opaque.meta` text record (needs [OpaqueClientConfig.ens](../interfaces/OpaqueClientConfig.md#ens)) |
| `*.sol` | SNS Records V2 TXT record (needs [OpaqueClientConfig.solana](../interfaces/OpaqueClientConfig.md#solana) or `sns.getRecord`) |

Every path point-validates both 33-byte halves before returning. Throws with a
path-specific message when the identity is unregistered, unset, or malformed.

#### Parameters

##### input

`string`

#### Returns

`Promise`\<[`ResolvedRecipient`](../interfaces/ResolvedRecipient.md)\>

***

### resolveRecipientMetaAddress()

> **resolveRecipientMetaAddress**(`recipientAddress`): `Promise`\<[`ResolveRecipientMetaResult`](../interfaces/ResolveRecipientMetaResult.md)\>

Defined in: [packages/opaque/src/client.ts:728](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L728)

Look up a recipient’s stealth meta-address on `StealthMetaAddressRegistry` using this client’s
`rpcUrl` and configured registry (scheme id [EIP5564\_SCHEME\_SECP256K1](../variables/EIP5564_SCHEME_SECP256K1.md)).

When the account has not registered, `registered` is false and `metaAddressHex` is omitted —
`recipientAddress` is still the checksummed address you passed in so you can show “not on Opaque yet”.

#### Parameters

##### recipientAddress

`` `0x${string}` ``

Normal Ethereum address of the intended recipient.

#### Returns

`Promise`\<[`ResolveRecipientMetaResult`](../interfaces/ResolveRecipientMetaResult.md)\>

***

### scan()

> **scan**(`opts`): `Promise`\<[`UnifiedOwnedOutput`](../interfaces/UnifiedOwnedOutput.md)[]\>

Defined in: [packages/opaque/src/client.ts:1455](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1455)

Scan one or more chains for stealth outputs owned by this wallet and return a single,
merged inbox. Each chain's native announcements are fetched through its [ChainAdapter](../interfaces/ChainAdapter.md)
and run through the same WASM view-tag + DKSAP filter ([filterOwnedAnnouncements](#filterownedannouncements)), so
detection is identical across chains. Outputs are tagged with their source `chain` / `chainId`.

`"ethereum"` reuses this client's viem client + configured announcer/registry. `"solana"`
requires [OpaqueClientConfig.solana](../interfaces/OpaqueClientConfig.md#solana) (connection / rpcUrl / cluster; defaults to devnet).
The viewing/spending keys are chain-neutral, so one wallet's inbox spans both chains.

#### Parameters

##### opts

###### chains

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)[]

###### fromBlock?

`bigint`

Lower-bound cursor: EVM block number (Solana scans the most recent signatures).

###### includeCrossChain?

`boolean`

Also merge cross-chain (UAB) announcements, tagged `source: "uab"`: on Ethereum, events
re-emitted by the EVM UABReceiver; on Solana, `CrossChainAnnouncement` events from the
`uab-receiver` program (merged by the adapter). Defaults to `true` wherever a UAB
deployment is configured; set `false` to skip, or `true` to force on the EVM side
(throws if UAB is unconfigured there).

###### solanaLimit?

`number`

Max Solana signatures to scan (adapter default when omitted).

###### toBlock?

`bigint`

Upper-bound EVM block; omit for the chain tip.

#### Returns

`Promise`\<[`UnifiedOwnedOutput`](../interfaces/UnifiedOwnedOutput.md)[]\>

***

### scanCrossChain()

> **scanCrossChain**(`opts?`): `Promise`\<[`OwnedStealthOutput`](../interfaces/OwnedStealthOutput.md)[]\>

Defined in: [packages/opaque/src/client.ts:1382](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1382)

Discover stealth outputs owned by this user that arrived via the cross-chain UAB.

#### Parameters

##### opts?

###### fromBlock?

`bigint`

###### toBlock?

`bigint` \| `"latest"`

#### Returns

`Promise`\<[`OwnedStealthOutput`](../interfaces/OwnedStealthOutput.md)[]\>

***

### sendStealthPayment()

> **sendStealthPayment**(`params`): `Promise`\<[`SendStealthPaymentResult`](../interfaces/SendStealthPaymentResult.md)\>

Defined in: [packages/opaque/src/client.ts:1017](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1017)

High-level send: resolve the recipient, derive a one-time stealth destination, transfer the
native asset, and publish the discovery announcement — in one call, dispatching on `chain`.

Solana bundles the transfer and `announce` (or `announce_with_relay` when `relay` is set) into a
single transaction and returns its signature. Ethereum submits the value transfer first, then
the announce, returning both tx hashes. Token (SPL/ERC-20) sends are not yet supported.
Requires the chain's signer (`solanaWallet` / `ethereumWalletClient` or `ethereumProvider`).

#### Parameters

##### params

[`SendStealthPaymentParams`](../interfaces/SendStealthPaymentParams.md)

#### Returns

`Promise`\<[`SendStealthPaymentResult`](../interfaces/SendStealthPaymentResult.md)\>

***

### simulateReputationVerification()

> **simulateReputationVerification**\<`TTransport`, `TChain`, `TAccount`\>(`wallet`, `args`): `Promise`\<`void`\>

Defined in: [packages/opaque/src/client.ts:2299](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2299)

Simulate `verifyReputation` for gas / revert checks.

#### Type Parameters

##### TTransport

`TTransport` *extends* `Transport`

##### TChain

`TChain` *extends* `Chain`

##### TAccount

`TAccount` *extends* `Account` \| `undefined`

#### Parameters

##### wallet

###### account

`TAccount`

The Account of the Client.

###### addChain

(`args`) => `Promise`\<`void`\>

Adds an EVM chain to the wallet.

- Docs: https://viem.sh/docs/actions/wallet/addChain
- JSON-RPC Methods: [`eth_addEthereumChain`](https://eips.ethereum.org/EIPS/eip-3085)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { optimism } from 'viem/chains'

const client = createWalletClient({
  transport: custom(window.ethereum),
})
await client.addChain({ chain: optimism })
```

###### batch?

\{ `multicall?`: `boolean` \| \{ `batchSize?`: `number`; `deployless?`: `boolean`; `wait?`: `number`; \}; \}

Flags for batch settings.

###### batch.multicall?

`boolean` \| \{ `batchSize?`: `number`; `deployless?`: `boolean`; `wait?`: `number`; \}

Toggle to enable `eth_call` multicall aggregation.

###### cacheTime

`number`

Time (in ms) that cached data will remain in memory.

###### ccipRead?

`false` \| \{ `request?`: (`parameters`) => `Promise`\<`` `0x${string}` ``\>; \}

[CCIP Read](https://eips.ethereum.org/EIPS/eip-3668) configuration.

###### chain

`TChain`

Chain for the client.

###### dataSuffix?

`DataSuffix`

Data suffix to append to transaction data.

###### deployContract

\<`abi`, `chainOverride`\>(`args`) => `Promise`\<`` `0x${string}` ``\>

Deploys a contract to the network, given bytecode and constructor arguments.

- Docs: https://viem.sh/docs/contract/deployContract
- Examples: https://stackblitz.com/github/wevm/viem/tree/main/examples/contracts_deploying-contracts

**Example**

```ts
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})
const hash = await client.deployContract({
  abi: [],
  account: '0x…,
  bytecode: '0x608060405260405161083e38038061083e833981016040819052610...',
})
```

###### experimental_blockTag?

`BlockTag`

Default block tag to use for RPC requests.

###### extend

\<`client`\>(`fn`) => `Client`\<`TTransport`, `TChain`, `TAccount`, `WalletRpcSchema`, \{ \[K in string \| number \| symbol\]: client\[K\] \} & `WalletActions`\<`TChain`, `TAccount`\>\>

###### fillTransaction

\<`chainOverride`, `accountOverride`\>(`args`) => `Promise`\<`FillTransactionReturnType`\<`TChain`, `chainOverride`\>\>

Fills a transaction request with the necessary fields to be signed over.

- Docs: https://viem.sh/docs/actions/public/fillTransaction

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const result = await client.fillTransaction({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
  value: parseEther('1'),
})
```

###### getAddresses

() => `Promise`\<`GetAddressesReturnType`\>

Returns a list of account addresses owned by the wallet or client.

- Docs: https://viem.sh/docs/actions/wallet/getAddresses
- JSON-RPC Methods: [`eth_accounts`](https://ethereum.org/en/developers/docs/apis/json-rpc/#eth_accounts)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const accounts = await client.getAddresses()
```

###### getCallsStatus

(`parameters`) => `Promise`\<\{ `atomic`: `boolean`; `capabilities?`: \{\[`key`: `string`\]: `any`; \} \| \{\[`key`: `string`\]: `any`; \}; `chainId`: `number`; `id`: `string`; `receipts?`: `WalletCallReceipt`\<`bigint`, `"success"` \| `"reverted"`\>[]; `status`: `"success"` \| `"pending"` \| `"failure"` \| `undefined`; `statusCode`: `number`; `version`: `string`; \}\>

Returns the status of a call batch that was sent via `sendCalls`.

- Docs: https://viem.sh/docs/actions/wallet/getCallsStatus
- JSON-RPC Methods: [`wallet_getCallsStatus`](https://eips.ethereum.org/EIPS/eip-5792)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const { receipts, status } = await client.getCallsStatus({ id: '0xdeadbeef' })
```

###### getCapabilities

\<`chainId`\>(`parameters?`) => `Promise`\<\{ \[K in string \| number \| symbol\]: (chainId extends number ? \{ atomic?: \{ status: "supported" \| "ready" \| "unsupported" \}; paymasterService?: \{ supported: boolean \}; unstable\_addSubAccount?: \{ keyTypes: ((...) \| (...) \| (...) \| (...))\[\]; supported: boolean \}; \[key: string\]: any \} : ChainIdToCapabilities\<Capabilities\<\{ atomic?: \{ status: ... \}; paymasterService?: \{ supported: ... \}; unstable\_addSubAccount?: \{ keyTypes: ...; supported: ... \}; \[key: string\]: any \}\>, number\>)\[K\] \}\>

Extract capabilities that a connected wallet supports (e.g. paymasters, session keys, etc).

- Docs: https://viem.sh/docs/actions/wallet/getCapabilities
- JSON-RPC Methods: [`wallet_getCapabilities`](https://eips.ethereum.org/EIPS/eip-5792)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const capabilities = await client.getCapabilities({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
})
```

###### getChainId

() => `Promise`\<`number`\>

Returns the chain ID associated with the current network.

- Docs: https://viem.sh/docs/actions/public/getChainId
- JSON-RPC Methods: [`eth_chainId`](https://ethereum.org/en/developers/docs/apis/json-rpc/#eth_chainid)

**Example**

```ts
import { createWalletClient, http } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const chainId = await client.getChainId()
// 1
```

###### getPermissions

() => `Promise`\<`GetPermissionsReturnType`\>

Gets the wallets current permissions.

- Docs: https://viem.sh/docs/actions/wallet/getPermissions
- JSON-RPC Methods: [`wallet_getPermissions`](https://eips.ethereum.org/EIPS/eip-2255)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const permissions = await client.getPermissions()
```

###### key

`string`

A key for the client.

###### name

`string`

A name for the client.

###### pollingInterval

`number`

Frequency (in ms) for polling enabled actions & events. Defaults to 4_000 milliseconds.

###### prepareAuthorization

(`parameters`) => `Promise`\<`PrepareAuthorizationReturnType`\>

Prepares an [EIP-7702 Authorization](https://eips.ethereum.org/EIPS/eip-7702) object for signing.
This Action will fill the required fields of the Authorization object if they are not provided (e.g. `nonce` and `chainId`).

With the prepared Authorization object, you can use [`signAuthorization`](https://viem.sh/docs/eip7702/signAuthorization) to sign over the Authorization object.

**Examples**

```ts
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: http(),
})

const authorization = await client.prepareAuthorization({
  account: privateKeyToAccount('0x..'),
  contractAddress: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})

const authorization = await client.prepareAuthorization({
  contractAddress: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
})
```

###### prepareTransactionRequest

\<`request`, `chainOverride`, `accountOverride`\>(`args`) => `Promise`\<\{ \[K in string \| number \| symbol\]: (UnionRequiredBy\<Extract\<UnionOmit\<(...), (...)\> & ((...) extends (...) ? (...) : (...)) & ((...) extends (...) ? (...) : (...)), IsNever\<(...)\> extends true ? unknown : ExactPartial\<(...)\>\> & \{ chainId?: number \}, ParameterTypeToParameters\<request\["parameters"\] extends readonly PrepareTransactionRequestParameterType\[\] ? any\[any\]\[number\] : "type" \| "chainId" \| "gas" \| "nonce" \| "blobVersionedHashes" \| "fees"\>\> & (unknown extends request\["kzg"\] ? \{\} : Pick\<request, "kzg"\>))\[K\] \}\>

Prepares a transaction request for signing.

- Docs: https://viem.sh/docs/actions/wallet/prepareTransactionRequest

**Examples**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const request = await client.prepareTransactionRequest({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  to: '0x0000000000000000000000000000000000000000',
  value: 1n,
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: custom(window.ethereum),
})
const request = await client.prepareTransactionRequest({
  to: '0x0000000000000000000000000000000000000000',
  value: 1n,
})
```

###### request

`EIP1193RequestFn`\<`WalletRpcSchema`\>

Request function wrapped with friendly error handling

###### requestAddresses

() => `Promise`\<`RequestAddressesReturnType`\>

Requests a list of accounts managed by a wallet.

- Docs: https://viem.sh/docs/actions/wallet/requestAddresses
- JSON-RPC Methods: [`eth_requestAccounts`](https://eips.ethereum.org/EIPS/eip-1102)

Sends a request to the wallet, asking for permission to access the user's accounts. After the user accepts the request, it will return a list of accounts (addresses).

This API can be useful for dapps that need to access the user's accounts in order to execute transactions or interact with smart contracts.

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const accounts = await client.requestAddresses()
```

###### requestPermissions

(`args`) => `Promise`\<`RequestPermissionsReturnType`\>

Requests permissions for a wallet.

- Docs: https://viem.sh/docs/actions/wallet/requestPermissions
- JSON-RPC Methods: [`wallet_requestPermissions`](https://eips.ethereum.org/EIPS/eip-2255)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const permissions = await client.requestPermissions({
  eth_accounts: {}
})
```

###### sendCalls

\<`calls`, `chainOverride`\>(`parameters`) => `Promise`\<\{ `capabilities?`: \{\[`key`: `string`\]: `any`; \}; `id`: `string`; \}\>

Requests the connected wallet to send a batch of calls.

- Docs: https://viem.sh/docs/actions/wallet/sendCalls
- JSON-RPC Methods: [`wallet_sendCalls`](https://eips.ethereum.org/EIPS/eip-5792)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const id = await client.sendCalls({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  calls: [
    {
      data: '0xdeadbeef',
      to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
    },
    {
      to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
      value: 69420n,
    },
  ],
})
```

###### sendCallsSync

\<`calls`, `chainOverride`\>(`parameters`) => `Promise`\<\{ `atomic`: `boolean`; `capabilities?`: \{\[`key`: `string`\]: `any`; \} \| \{\[`key`: `string`\]: `any`; \}; `chainId`: `number`; `id`: `string`; `receipts?`: `WalletCallReceipt`\<`bigint`, `"success"` \| `"reverted"`\>[]; `status`: `"success"` \| `"pending"` \| `"failure"` \| `undefined`; `statusCode`: `number`; `version`: `string`; \}\>

Requests the connected wallet to send a batch of calls, and waits for the calls to be included in a block.

- Docs: https://viem.sh/docs/actions/wallet/sendCallsSync
- JSON-RPC Methods: [`wallet_sendCalls`](https://eips.ethereum.org/EIPS/eip-5792)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const status = await client.sendCallsSync({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  calls: [
    {
      data: '0xdeadbeef',
      to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
    },
    {
      to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
      value: 69420n,
    },
  ],
})
```

###### sendRawTransaction

(`args`) => `Promise`\<`` `0x${string}` ``\>

Sends a **signed** transaction to the network

- Docs: https://viem.sh/docs/actions/wallet/sendRawTransaction
- JSON-RPC Method: [`eth_sendRawTransaction`](https://ethereum.github.io/execution-apis/api-documentation/)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'
import { sendRawTransaction } from 'viem/wallet'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const hash = await client.sendRawTransaction({
  serializedTransaction: '0x02f850018203118080825208808080c080a04012522854168b27e5dc3d5839bab5e6b39e1a0ffd343901ce1622e3d64b48f1a04e00902ae0502c4728cbf12156290df99c3ed7de85b1dbfe20b5c36931733a33'
})
```

###### sendRawTransactionSync

(`args`) => `Promise`\<`ExtractChainFormatterReturnType`\<`TChain`, `"transactionReceipt"`, `TransactionReceipt`\>\>

Sends a **signed** transaction to the network synchronously,
and waits for the transaction to be included in a block.

- Docs: https://viem.sh/docs/actions/wallet/sendRawTransactionSync
- JSON-RPC Method: [`eth_sendRawTransactionSync`](https://eips.ethereum.org/EIPS/eip-7966)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'
import { sendRawTransactionSync } from 'viem/wallet'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const receipt = await client.sendRawTransactionSync({
  serializedTransaction: '0x02f850018203118080825208808080c080a04012522854168b27e5dc3d5839bab5e6b39e1a0ffd343901ce1622e3d64b48f1a04e00902ae0502c4728cbf12156290df99c3ed7de85b1dbfe20b5c36931733a33'
})
```

###### sendTransaction

\<`request`, `chainOverride`\>(`args`) => `Promise`\<`` `0x${string}` ``\>

Creates, signs, and sends a new transaction to the network.

- Docs: https://viem.sh/docs/actions/wallet/sendTransaction
- Examples: https://stackblitz.com/github/wevm/viem/tree/main/examples/transactions_sending-transactions
- JSON-RPC Methods:
  - JSON-RPC Accounts: [`eth_sendTransaction`](https://ethereum.org/en/developers/docs/apis/json-rpc/#eth_sendtransaction)
  - Local Accounts: [`eth_sendRawTransaction`](https://ethereum.org/en/developers/docs/apis/json-rpc/#eth_sendrawtransaction)

**Examples**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const hash = await client.sendTransaction({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
  value: 1000000000000000000n,
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})
const hash = await client.sendTransaction({
  to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
  value: 1000000000000000000n,
})
```

###### sendTransactionSync

\<`request`, `chainOverride`\>(`args`) => `Promise`\<`ExtractChainFormatterReturnType`\<`TChain`, `"transactionReceipt"`, `TransactionReceipt`\>\>

Creates, signs, and sends a new transaction to the network synchronously.
Returns the transaction receipt.

- Docs: https://viem.sh/docs/actions/wallet/sendTransactionSync
- Examples: https://stackblitz.com/github/wevm/viem/tree/main/examples/transactions_sending-transactions
- JSON-RPC Methods:
  - JSON-RPC Accounts: [`eth_sendTransaction`](https://ethereum.org/en/developers/docs/apis/json-rpc/#eth_sendtransaction)
  - Local Accounts: [`eth_sendRawTransaction`](https://ethereum.org/en/developers/docs/apis/json-rpc/#eth_sendrawtransaction)

**Examples**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const receipt = await client.sendTransactionSync({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
  value: 1000000000000000000n,
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})
const receipt = await client.sendTransactionSync({
  to: '0x70997970c51812dc3a010c7d01b50e0d17dc79c8',
  value: 1000000000000000000n,
})
```

###### showCallsStatus

(`parameters`) => `Promise`\<`void`\>

Requests for the wallet to show information about a call batch
that was sent via `sendCalls`.

- Docs: https://viem.sh/docs/actions/wallet/showCallsStatus
- JSON-RPC Methods: [`wallet_showCallsStatus`](https://eips.ethereum.org/EIPS/eip-5792)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

await client.showCallsStatus({ id: '0xdeadbeef' })
```

###### signAuthorization

(`parameters`) => `Promise`\<`SignAuthorizationReturnType`\>

Signs an [EIP-7702 Authorization](https://eips.ethereum.org/EIPS/eip-7702) object.

With the calculated signature, you can:
- use [`verifyAuthorization`](https://viem.sh/docs/eip7702/verifyAuthorization) to verify the signed Authorization object,
- use [`recoverAuthorizationAddress`](https://viem.sh/docs/eip7702/recoverAuthorizationAddress) to recover the signing address from the signed Authorization object.

**Examples**

```ts
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: http(),
})

const signature = await client.signAuthorization({
  account: privateKeyToAccount('0x..'),
  contractAddress: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})

const signature = await client.signAuthorization({
  contractAddress: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
})
```

###### signMessage

(`args`) => `Promise`\<`` `0x${string}` ``\>

Calculates an Ethereum-specific signature in [EIP-191 format](https://eips.ethereum.org/EIPS/eip-191): `keccak256("\x19Ethereum Signed Message:\n" + len(message) + message))`.

- Docs: https://viem.sh/docs/actions/wallet/signMessage
- JSON-RPC Methods:
  - JSON-RPC Accounts: [`personal_sign`](https://docs.metamask.io/guide/signing-data#personal-sign)
  - Local Accounts: Signs locally. No JSON-RPC request.

With the calculated signature, you can:
- use [`verifyMessage`](https://viem.sh/docs/utilities/verifyMessage) to verify the signature,
- use [`recoverMessageAddress`](https://viem.sh/docs/utilities/recoverMessageAddress) to recover the signing address from a signature.

**Examples**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const signature = await client.signMessage({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  message: 'hello world',
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})
const signature = await client.signMessage({
  message: 'hello world',
})
```

###### signTransaction

\<`chainOverride`, `request`\>(`args`) => `Promise`\<`TransactionSerialized`\<`GetTransactionType`\<`request`, `request` *extends* `LegacyProperties` ? `"legacy"` : `never` \| `request` *extends* `EIP1559Properties` ? `"eip1559"` : `never` \| `request` *extends* `EIP2930Properties` ? `"eip2930"` : `never` \| `request` *extends* `EIP4844Properties` ? `"eip4844"` : `never` \| `request` *extends* `EIP7702Properties` ? `"eip7702"` : `never` \| `request`\[`"type"`\] *extends* `string` \| `undefined` ? `Extract`\<`any`\[`any`\], `string`\> : `never`\>, `GetTransactionType`\<`request`, `request` *extends* `LegacyProperties` ? `"legacy"` : `never` \| `request` *extends* `EIP1559Properties` ? `"eip1559"` : `never` \| `request` *extends* `EIP2930Properties` ? `"eip2930"` : `never` \| `request` *extends* `EIP4844Properties` ? `"eip4844"` : `never` \| `request` *extends* `EIP7702Properties` ? `"eip7702"` : `never` \| `request`\[`"type"`\] *extends* `string` \| `undefined` ? `Extract`\<`any`\[`any`\], `string`\> : `never`\> *extends* `"eip1559"` ? `` `0x02${string}` `` : `never` \| `GetTransactionType`\<`request`, `request` *extends* `LegacyProperties` ? `"legacy"` : `never` \| `request` *extends* `EIP1559Properties` ? `"eip1559"` : `never` \| `request` *extends* `EIP2930Properties` ? `"eip2930"` : `never` \| `request` *extends* `EIP4844Properties` ? `"eip4844"` : `never` \| `request` *extends* `EIP7702Properties` ? `"eip7702"` : `never` \| `request`\[`"type"`\] *extends* `string` \| `undefined` ? `Extract`\<`any`\[`any`\], `string`\> : `never`\> *extends* `"eip2930"` ? `` `0x01${string}` `` : `never` \| `GetTransactionType`\<`request`, `request` *extends* `LegacyProperties` ? `"legacy"` : `never` \| `request` *extends* `EIP1559Properties` ? `"eip1559"` : `never` \| `request` *extends* `EIP2930Properties` ? `"eip2930"` : `never` \| `request` *extends* `EIP4844Properties` ? `"eip4844"` : `never` \| `request` *extends* `EIP7702Properties` ? `"eip7702"` : `never` \| `request`\[`"type"`\] *extends* `string` \| `undefined` ? `Extract`\<`any`\[`any`\], `string`\> : `never`\> *extends* `"eip4844"` ? `` `0x03${string}` `` : `never` \| `GetTransactionType`\<`request`, `request` *extends* `LegacyProperties` ? `"legacy"` : `never` \| `request` *extends* `EIP1559Properties` ? `"eip1559"` : `never` \| `request` *extends* `EIP2930Properties` ? `"eip2930"` : `never` \| `request` *extends* `EIP4844Properties` ? `"eip4844"` : `never` \| `request` *extends* `EIP7702Properties` ? `"eip7702"` : `never` \| `request`\[`"type"`\] *extends* `string` \| `undefined` ? `Extract`\<`any`\[`any`\], `string`\> : `never`\> *extends* `"eip7702"` ? `` `0x04${string}` `` : `never` \| `GetTransactionType`\<`request`, `request` *extends* `LegacyProperties` ? `"legacy"` : `never` \| `request` *extends* `EIP1559Properties` ? `"eip1559"` : `never` \| `request` *extends* `EIP2930Properties` ? `"eip2930"` : `never` \| `request` *extends* `EIP4844Properties` ? `"eip4844"` : `never` \| `request` *extends* `EIP7702Properties` ? `"eip7702"` : `never` \| `request`\[`"type"`\] *extends* `string` \| `undefined` ? `Extract`\<`any`\[`any`\], `string`\> : `never`\> *extends* `"legacy"` ? `TransactionSerializedLegacy` : `never`\>\>

Signs a transaction.

- Docs: https://viem.sh/docs/actions/wallet/signTransaction
- JSON-RPC Methods:
  - JSON-RPC Accounts: [`eth_signTransaction`](https://ethereum.github.io/execution-apis/api-documentation/)
  - Local Accounts: Signs locally. No JSON-RPC request.

**Examples**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const request = await client.prepareTransactionRequest({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  to: '0x0000000000000000000000000000000000000000',
  value: 1n,
})
const signature = await client.signTransaction(request)
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: custom(window.ethereum),
})
const request = await client.prepareTransactionRequest({
  to: '0x0000000000000000000000000000000000000000',
  value: 1n,
})
const signature = await client.signTransaction(request)
```

###### signTypedData

\<`typedData`, `primaryType`\>(`args`) => `Promise`\<`` `0x${string}` ``\>

Signs typed data and calculates an Ethereum-specific signature in [EIP-191 format](https://eips.ethereum.org/EIPS/eip-191): `keccak256("\x19Ethereum Signed Message:\n" + len(message) + message))`.

- Docs: https://viem.sh/docs/actions/wallet/signTypedData
- JSON-RPC Methods:
  - JSON-RPC Accounts: [`eth_signTypedData_v4`](https://docs.metamask.io/guide/signing-data#signtypeddata-v4)
  - Local Accounts: Signs locally. No JSON-RPC request.

**Examples**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const signature = await client.signTypedData({
  account: '0xA0Cf798816D4b9b9866b5330EEa46a18382f251e',
  domain: {
    name: 'Ether Mail',
    version: '1',
    chainId: 1,
    verifyingContract: '0xCcCCccccCCCCcCCCCCCcCcCccCcCCCcCcccccccC',
  },
  types: {
    Person: [
      { name: 'name', type: 'string' },
      { name: 'wallet', type: 'address' },
    ],
    Mail: [
      { name: 'from', type: 'Person' },
      { name: 'to', type: 'Person' },
      { name: 'contents', type: 'string' },
    ],
  },
  primaryType: 'Mail',
  message: {
    from: {
      name: 'Cow',
      wallet: '0xCD2a3d9F938E13CD947Ec05AbC7FE734Df8DD826',
    },
    to: {
      name: 'Bob',
      wallet: '0xbBbBBBBbbBBBbbbBbbBbbbbBBbBbbbbBbBbbBBbB',
    },
    contents: 'Hello, Bob!',
  },
})
```

```ts
// Account Hoisting
import { createWalletClient, http } from 'viem'
import { privateKeyToAccount } from 'viem/accounts'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  account: privateKeyToAccount('0x…'),
  chain: mainnet,
  transport: http(),
})
const signature = await client.signTypedData({
  domain: {
    name: 'Ether Mail',
    version: '1',
    chainId: 1,
    verifyingContract: '0xCcCCccccCCCCcCCCCCCcCcCccCcCCCcCcccccccC',
  },
  types: {
    Person: [
      { name: 'name', type: 'string' },
      { name: 'wallet', type: 'address' },
    ],
    Mail: [
      { name: 'from', type: 'Person' },
      { name: 'to', type: 'Person' },
      { name: 'contents', type: 'string' },
    ],
  },
  primaryType: 'Mail',
  message: {
    from: {
      name: 'Cow',
      wallet: '0xCD2a3d9F938E13CD947Ec05AbC7FE734Df8DD826',
    },
    to: {
      name: 'Bob',
      wallet: '0xbBbBBBBbbBBBbbbBbbBbbbbBBbBbbbbBbBbbBBbB',
    },
    contents: 'Hello, Bob!',
  },
})
```

###### switchChain

(`args`) => `Promise`\<`void`\>

Switch the target chain in a wallet.

- Docs: https://viem.sh/docs/actions/wallet/switchChain
- JSON-RPC Methods: [`eth_switchEthereumChain`](https://eips.ethereum.org/EIPS/eip-3326)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet, optimism } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
await client.switchChain({ id: optimism.id })
```

###### transport

`ReturnType`\<`TTransport`\>\[`"config"`\] & `ReturnType`\<`TTransport`\>\[`"value"`\]

The RPC transport

###### type

`string`

The type of client.

###### uid

`string`

A unique ID for the client.

###### waitForCallsStatus

(`parameters`) => `Promise`\<\{ `atomic`: `boolean`; `capabilities?`: \{\[`key`: `string`\]: `any`; \} \| \{\[`key`: `string`\]: `any`; \}; `chainId`: `number`; `id`: `string`; `receipts?`: `WalletCallReceipt`\<`bigint`, `"success"` \| `"reverted"`\>[]; `status`: `"success"` \| `"pending"` \| `"failure"` \| `undefined`; `statusCode`: `number`; `version`: `string`; \}\>

Waits for the status & receipts of a call bundle that was sent via `sendCalls`.

- Docs: https://viem.sh/docs/actions/wallet/waitForCallsStatus
- JSON-RPC Methods: [`wallet_getCallsStatus`](https://eips.ethereum.org/EIPS/eip-5792)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})

const { receipts, status } = await waitForCallsStatus(client, { id: '0xdeadbeef' })
```

###### watchAsset

(`args`) => `Promise`\<`boolean`\>

Adds an EVM chain to the wallet.

- Docs: https://viem.sh/docs/actions/wallet/watchAsset
- JSON-RPC Methods: [`eth_switchEthereumChain`](https://eips.ethereum.org/EIPS/eip-747)

**Example**

```ts
import { createWalletClient, custom } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const success = await client.watchAsset({
  type: 'ERC20',
  options: {
    address: '0xc02aaa39b223fe8d0a0e5c4f27ead9083c756cc2',
    decimals: 18,
    symbol: 'WETH',
  },
})
```

###### writeContract

\<`abi`, `functionName`, `args`, `chainOverride`\>(`args`) => `Promise`\<`` `0x${string}` ``\>

Executes a write function on a contract.

- Docs: https://viem.sh/docs/contract/writeContract
- Examples: https://stackblitz.com/github/wevm/viem/tree/main/examples/contracts_writing-to-contracts

A "write" function on a Solidity contract modifies the state of the blockchain. These types of functions require gas to be executed, and hence a [Transaction](https://viem.sh/docs/glossary/terms) is needed to be broadcast in order to change the state.

Internally, uses a [Wallet Client](https://viem.sh/docs/clients/wallet) to call the [`sendTransaction` action](https://viem.sh/docs/actions/wallet/sendTransaction) with [ABI-encoded `data`](https://viem.sh/docs/contract/encodeFunctionData).

__Warning: The `write` internally sends a transaction – it does not validate if the contract write will succeed (the contract may throw an error). It is highly recommended to [simulate the contract write with `contract.simulate`](https://viem.sh/docs/contract/writeContract#usage) before you execute it.__

**Examples**

```ts
import { createWalletClient, custom, parseAbi } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const hash = await client.writeContract({
  address: '0xFBA3912Ca04dd458c843e2EE08967fC04f3579c2',
  abi: parseAbi(['function mint(uint32 tokenId) nonpayable']),
  functionName: 'mint',
  args: [69420],
})
```

```ts
// With Validation
import { createWalletClient, custom, parseAbi } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const { request } = await client.simulateContract({
  address: '0xFBA3912Ca04dd458c843e2EE08967fC04f3579c2',
  abi: parseAbi(['function mint(uint32 tokenId) nonpayable']),
  functionName: 'mint',
  args: [69420],
}
const hash = await client.writeContract(request)
```

###### writeContractSync

\<`abi`, `functionName`, `args`, `chainOverride`\>(`args`) => `Promise`\<`TransactionReceipt`\>

Executes a write function on a contract synchronously.
Returns the transaction receipt.

- Docs: https://viem.sh/docs/contract/writeContract

A "write" function on a Solidity contract modifies the state of the blockchain. These types of functions require gas to be executed, and hence a [Transaction](https://viem.sh/docs/glossary/terms) is needed to be broadcast in order to change the state.

Internally, uses a [Wallet Client](https://viem.sh/docs/clients/wallet) to call the [`sendTransaction` action](https://viem.sh/docs/actions/wallet/sendTransaction) with [ABI-encoded `data`](https://viem.sh/docs/contract/encodeFunctionData).

__Warning: The `write` internally sends a transaction – it does not validate if the contract write will succeed (the contract may throw an error). It is highly recommended to [simulate the contract write with `contract.simulate`](https://viem.sh/docs/contract/writeContract#usage) before you execute it.__

**Example**

```ts
import { createWalletClient, custom, parseAbi } from 'viem'
import { mainnet } from 'viem/chains'

const client = createWalletClient({
  chain: mainnet,
  transport: custom(window.ethereum),
})
const receipt = await client.writeContractSync({
  address: '0xFBA3912Ca04dd458c843e2EE08967fC04f3579c2',
  abi: parseAbi(['function mint(uint32 tokenId) nonpayable']),
  functionName: 'mint',
  args: [69420],
})
```

##### args

[`VerifyReputationArgs`](../interfaces/VerifyReputationArgs.md)

#### Returns

`Promise`\<`void`\>

***

### submitReputationVerification()

> **submitReputationVerification**(`chain`, `args`): `Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

Defined in: [packages/opaque/src/client.ts:2321](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2321)

Broadcast a reputation proof to the verifier, dispatching on `chain` (consumes the nullifier on
success). Uses the configured signer for each chain — `ethereumWalletClient` / `ethereumProvider`
for Ethereum, `solanaWallet` for Solana. The same [VerifyReputationArgs](../interfaces/VerifyReputationArgs.md) feeds both:
`proofData` (from [generateReputationProof](#generatereputationproof)), `merkleRoot`, and `externalNullifier`.

#### Parameters

##### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

##### args

[`VerifyReputationArgs`](../interfaces/VerifyReputationArgs.md)

#### Returns

`Promise`\<[`PsrTxResult`](../interfaces/PsrTxResult.md)\>

***

### sweep()

> **sweep**(`params`): `Promise`\<\{ `chain`: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md); `tx`: `string`; \}\>

Defined in: [packages/opaque/src/client.ts:1575](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L1575)

Sweep the full native balance of an owned stealth output to `destination`, signed by the
reconstructed one-time key (the on-chain `from` is the stealth address itself). Works for
Ethereum (ETH) and Solana (SOL); `"solana"` requires [OpaqueClientConfig.solana](../interfaces/OpaqueClientConfig.md#solana).

#### Parameters

##### params

###### chain

[`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md)

###### destination

`string`

###### output

`Pick`\<[`OwnedStealthOutput`](../interfaces/OwnedStealthOutput.md), `"ephemeralPublicKey"`\>

#### Returns

`Promise`\<\{ `chain`: [`OpaqueScanChain`](../type-aliases/OpaqueScanChain.md); `tx`: `string`; \}\>

***

### verifyReputationProofView()

> **verifyReputationProofView**(`args`): `Promise`\<`boolean`\>

Defined in: [packages/opaque/src/client.ts:2290](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2290)

On-chain view helper: verify proof without spending nullifier.

#### Parameters

##### args

[`VerifyReputationArgs`](../interfaces/VerifyReputationArgs.md)

#### Returns

`Promise`\<`boolean`\>

***

### chainDeployment()

> `static` **chainDeployment**(`chainId`): [`OpaqueChainDeployment`](../interfaces/OpaqueChainDeployment.md) \| `undefined`

Defined in: [packages/opaque/src/client.ts:2391](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2391)

Read bundled deployment metadata (contracts, default tokens) for a chain.

#### Parameters

##### chainId

`number`

#### Returns

[`OpaqueChainDeployment`](../interfaces/OpaqueChainDeployment.md) \| `undefined`

***

### create()

> `static` **create**(`config`): `Promise`\<`OpaqueClient`\>

Defined in: [packages/opaque/src/client.ts:614](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L614)

Construct a client: loads WASM, derives keys from `walletSignature`, wires RPC + addresses.

#### Parameters

##### config

[`OpaqueClientConfig`](../interfaces/OpaqueClientConfig.md)

#### Returns

`Promise`\<`OpaqueClient`\>

***

### fromWallet()

> `static` **fromWallet**(`params`): `Promise`\<`OpaqueClient`\>

Defined in: [packages/opaque/src/client.ts:648](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L648)

Construct a client from wallet(s) in the [UnifiedSigner](../type-aliases/UnifiedSigner.md) shape — the
one-adapter entry point for integrators (Phase 2.5). Pass at most one wallet per
chain; the FIRST wallet is prompted for the [SETUP\_MESSAGE](../variables/SETUP_MESSAGE.md) setup signature
(HKDF entropy) unless a cached `walletSignature` is supplied. Each wallet is also
wired as that chain's write signer (`ethereumProvider`/`ethereumWalletClient`,
`solanaWallet`), so PSR writes and sends work without further config.

#### Parameters

##### params

`Omit`\<[`OpaqueClientConfig`](../interfaces/OpaqueClientConfig.md), `"walletSignature"` \| `"ethereumAddress"` \| `"ethereumProvider"` \| `"ethereumWalletClient"` \| `"solanaWallet"`\> & `object`

#### Returns

`Promise`\<`OpaqueClient`\>

***

### supportedChainIds()

> `static` **supportedChainIds**(): `number`[]

Defined in: [packages/opaque/src/client.ts:2384](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L2384)

Chain IDs that ship with bundled contract addresses in this SDK version.

#### Returns

`number`[]
