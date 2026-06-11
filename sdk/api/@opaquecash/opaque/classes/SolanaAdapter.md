# Class: SolanaAdapter

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:24

Abstracts chain-specific announcement retrieval and registry reads so the universal
scan loop is written once. The universal scanner iterates a set of adapters, calls
[ChainAdapter.fetchAnnouncements](../interfaces/ChainAdapter.md#fetchannouncements), then runs the shared view-tag filter and DKSAP
recovery on the returned [Announcement](../interfaces/Announcement.md)s.

## Implements

- [`ChainAdapter`](../interfaces/ChainAdapter.md)

## Constructors

### Constructor

> **new SolanaAdapter**(`config?`): `SolanaAdapter`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:30

#### Parameters

##### config?

[`SolanaAdapterConfig`](../interfaces/SolanaAdapterConfig.md)

#### Returns

`SolanaAdapter`

## Properties

### chainId

> `readonly` **chainId**: `1` = `1`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:25

Wormhole chain id this adapter serves (Ethereum = 2, Solana = 1).

#### Implementation of

[`ChainAdapter`](../interfaces/ChainAdapter.md).[`chainId`](../interfaces/ChainAdapter.md#chainid)

***

### connection

> `readonly` **connection**: `Connection`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:27

***

### deployment

> `readonly` **deployment**: [`SolanaDeployment`](../interfaces/SolanaDeployment.md)

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:28

***

### name

> `readonly` **name**: `"solana"` = `"solana"`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:26

Human-readable adapter name, e.g. `"ethereum"` or `"solana"`.

#### Implementation of

[`ChainAdapter`](../interfaces/ChainAdapter.md).[`name`](../interfaces/ChainAdapter.md#name)

## Methods

### buildAnnounceInstruction()

> **buildAnnounceInstruction**(`params`): `TransactionInstruction`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:38

Build an `announce` instruction (the `caller` signs and pays).

#### Parameters

##### params

###### caller

`PublicKey`

###### ephemeralPubKey

`Uint8Array`

###### metadata

`Uint8Array`

###### schemeId?

`bigint`

###### stealthAddress

`Uint8Array`

#### Returns

`TransactionInstruction`

***

### buildAnnounceWithRelay()

> **buildAnnounceWithRelay**(`params`): `AnnounceWithRelayBuild`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:50

Build a cross-chain `announce_with_relay` instruction (emits locally AND relays over Wormhole)
plus the fresh message keypair that must co-sign the transaction. Resolves the announcer and
Wormhole core program ids from this adapter's deployment.

#### Parameters

##### params

###### batchId?

`number`

###### caller

`PublicKey`

###### ephemeralPubKey

`Uint8Array`

###### metadata

`Uint8Array`

###### schemeId?

`bigint`

###### stealthAddress

`Uint8Array`

###### wormholeFee?

`bigint`

#### Returns

`AnnounceWithRelayBuild`

***

### buildRegisterKeysInstruction()

> **buildRegisterKeysInstruction**(`registrant`, `stealthMetaAddress`, `schemeId?`): `TransactionInstruction`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:36

Build a `register_keys` instruction for `registrant`'s 66-byte meta-address.

#### Parameters

##### registrant

`PublicKey`

##### stealthMetaAddress

`Uint8Array`

##### schemeId?

`bigint`

#### Returns

`TransactionInstruction`

***

### fetchAnnouncements()

> **fetchAnnouncements**(`opts?`): `Promise`\<[`Announcement`](../interfaces/Announcement.md)[]\>

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:31

Fetch announcements in chain-neutral form (order is adapter-defined).

#### Parameters

##### opts?

[`FetchAnnouncementsOptions`](../interfaces/FetchAnnouncementsOptions.md)

#### Returns

`Promise`\<[`Announcement`](../interfaces/Announcement.md)[]\>

#### Implementation of

[`ChainAdapter`](../interfaces/ChainAdapter.md).[`fetchAnnouncements`](../interfaces/ChainAdapter.md#fetchannouncements)

***

### fetchWormholeMessageFee()

> **fetchWormholeMessageFee**(): `Promise`\<`bigint`\>

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:60

Current Wormhole message fee (lamports) for `announce_with_relay`; `0n` on devnet.

#### Returns

`Promise`\<`bigint`\>

***

### isRegistered()

> **isRegistered**(`identity`): `Promise`\<`boolean`\>

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:33

Whether `identity` has a stealth meta-address registered.

#### Parameters

##### identity

`string`

#### Returns

`Promise`\<`boolean`\>

#### Implementation of

[`ChainAdapter`](../interfaces/ChainAdapter.md).[`isRegistered`](../interfaces/ChainAdapter.md#isregistered)

***

### resolveMetaAddress()

> **resolveMetaAddress**(`identity`): `Promise`\<`` `0x${string}` `` \| `null`\>

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:32

Resolve an identity to its 66-byte stealth meta-address as `0x`-hex, or `null` when
unregistered. Identity is an EVM address (Ethereum) or a base58 pubkey (Solana).

#### Parameters

##### identity

`string`

#### Returns

`Promise`\<`` `0x${string}` `` \| `null`\>

#### Implementation of

[`ChainAdapter`](../interfaces/ChainAdapter.md).[`resolveMetaAddress`](../interfaces/ChainAdapter.md#resolvemetaaddress)

***

### sweepStealthSol()

> **sweepStealthSol**(`params`): `Promise`\<\{ `feeLamports`: `bigint`; `signature`: `string`; `sweepLamports`: `bigint`; \}\>

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:66

Sweep the full SOL balance of a one-time stealth account to `destination`. The stealth
keypair signs and pays its own fee; pass the reconstructed 32-byte secp256k1 stealth
private key (or the derived keypair).

#### Parameters

##### params

###### destination

`string` \| `PublicKey`

###### stealthKeypair?

`Keypair`

###### stealthPrivKey?

`Uint8Array`

#### Returns

`Promise`\<\{ `feeLamports`: `bigint`; `signature`: `string`; `sweepLamports`: `bigint`; \}\>

***

### watchAnnouncements()

> **watchAnnouncements**(`handlers`): () => `void`

Defined in: packages/stealth-chain-solana/dist/adapter.d.ts:34

Optional live subscription to new announcements; returns an unsubscribe function.

#### Parameters

##### handlers

[`AnnouncementHandlers`](../interfaces/AnnouncementHandlers.md)

#### Returns

() => `void`

#### Implementation of

[`ChainAdapter`](../interfaces/ChainAdapter.md).[`watchAnnouncements`](../interfaces/ChainAdapter.md#watchannouncements)
