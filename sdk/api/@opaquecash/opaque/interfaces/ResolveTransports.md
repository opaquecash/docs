# Interface: ResolveTransports

Defined in: [packages/opaque/src/resolve.ts:55](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L55)

Injectable transports for the off-chain resolution paths (all optional).

## Properties

### ensGetText?

> `optional` **ensGetText?**: (`name`, `key`) => `Promise`\<`string` \| `null`\>

Defined in: [packages/opaque/src/resolve.ts:60](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L60)

ENS text-record reader: returns the raw record value or `null` when unset.
Inject your own (e.g. viem `getEnsText` on a mainnet client, or a mock in tests).

#### Parameters

##### name

`string`

##### key

`string`

#### Returns

`Promise`\<`string` \| `null`\>

***

### fetchFn?

> `optional` **fetchFn?**: \{(`input`, `init?`): `Promise`\<`Response`\>; (`input`, `init?`): `Promise`\<`Response`\>; \}

Defined in: [packages/opaque/src/resolve.ts:64](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L64)

Fetch implementation for gateway requests (default `globalThis.fetch`).

#### Call Signature

> (`input`, `init?`): `Promise`\<`Response`\>

[MDN Reference](https://developer.mozilla.org/docs/Web/API/fetch)

##### Parameters

###### input

`URL` \| `RequestInfo`

###### init?

`RequestInit`

##### Returns

`Promise`\<`Response`\>

#### Call Signature

> (`input`, `init?`): `Promise`\<`Response`\>

[MDN Reference](https://developer.mozilla.org/docs/Web/API/fetch)

##### Parameters

###### input

`string` \| `URL` \| `Request`

###### init?

`RequestInit`

##### Returns

`Promise`\<`Response`\>

***

### ipfsGateways?

> `optional` **ipfsGateways?**: readonly `string`[]

Defined in: [packages/opaque/src/resolve.ts:62](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/resolve.ts#L62)

IPFS gateway base URLs tried in order (default [DEFAULT\_IPFS\_GATEWAYS](/sdk/api/@opaquecash/opaque/variables/DEFAULT_IPFS_GATEWAYS.md)).
