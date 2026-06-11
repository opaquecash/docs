# Interface: ChainAdapter

Defined in: packages/adapter/dist/index.d.ts:75

Abstracts chain-specific announcement retrieval and registry reads so the universal
scan loop is written once. The universal scanner iterates a set of adapters, calls
[ChainAdapter.fetchAnnouncements](#fetchannouncements), then runs the shared view-tag filter and DKSAP
recovery on the returned [Announcement](Announcement.md)s.

## Properties

### chainId

> `readonly` **chainId**: `number`

Defined in: packages/adapter/dist/index.d.ts:77

Wormhole chain id this adapter serves (Ethereum = 2, Solana = 1).

***

### name

> `readonly` **name**: `string`

Defined in: packages/adapter/dist/index.d.ts:79

Human-readable adapter name, e.g. `"ethereum"` or `"solana"`.

## Methods

### fetchAnnouncements()

> **fetchAnnouncements**(`opts?`): `Promise`\<[`Announcement`](Announcement.md)[]\>

Defined in: packages/adapter/dist/index.d.ts:81

Fetch announcements in chain-neutral form (order is adapter-defined).

#### Parameters

##### opts?

[`FetchAnnouncementsOptions`](FetchAnnouncementsOptions.md)

#### Returns

`Promise`\<[`Announcement`](Announcement.md)[]\>

***

### isRegistered()

> **isRegistered**(`identity`): `Promise`\<`boolean`\>

Defined in: packages/adapter/dist/index.d.ts:88

Whether `identity` has a stealth meta-address registered.

#### Parameters

##### identity

`string`

#### Returns

`Promise`\<`boolean`\>

***

### resolveMetaAddress()

> **resolveMetaAddress**(`identity`): `Promise`\<`` `0x${string}` `` \| `null`\>

Defined in: packages/adapter/dist/index.d.ts:86

Resolve an identity to its 66-byte stealth meta-address as `0x`-hex, or `null` when
unregistered. Identity is an EVM address (Ethereum) or a base58 pubkey (Solana).

#### Parameters

##### identity

`string`

#### Returns

`Promise`\<`` `0x${string}` `` \| `null`\>

***

### watchAnnouncements()?

> `optional` **watchAnnouncements**(`handlers`): () => `void`

Defined in: packages/adapter/dist/index.d.ts:90

Optional live subscription to new announcements; returns an unsubscribe function.

#### Parameters

##### handlers

[`AnnouncementHandlers`](AnnouncementHandlers.md)

#### Returns

() => `void`
