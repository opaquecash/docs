# Interface: SolanaUnifiedSigner

Defined in: [packages/opaque/src/signer.ts:25](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/signer.ts#L25)

A Solana wallet in unified shape (wallet-adapter compatible).

## Properties

### chain

> **chain**: `"solana"`

Defined in: [packages/opaque/src/signer.ts:26](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/signer.ts#L26)

***

### publicKey

> **publicKey**: `string` \| `PublicKey`

Defined in: [packages/opaque/src/signer.ts:27](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/signer.ts#L27)

***

### signMessage?

> `optional` **signMessage?**: (`message`) => `Promise`\<`Uint8Array`\>

Defined in: [packages/opaque/src/signer.ts:29](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/signer.ts#L29)

wallet-adapter `signMessage`; required only when this wallet derives the keys.

#### Parameters

##### message

`Uint8Array`

#### Returns

`Promise`\<`Uint8Array`\>

***

### signTransaction?

> `optional` **signTransaction?**: (`transaction`) => `Promise`\<`Transaction`\>

Defined in: [packages/opaque/src/signer.ts:31](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/signer.ts#L31)

wallet-adapter `signTransaction`; required for Solana writes.

#### Parameters

##### transaction

`Transaction`

#### Returns

`Promise`\<`Transaction`\>
