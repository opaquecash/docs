# Interface: PsrExpiryInput

Defined in: [packages/opaque/src/client.ts:297](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L297)

Future block (Ethereum) / slot (Solana) for a schema or attestation expiry.

## Properties

### dateTime?

> `optional` **dateTime?**: `string`

Defined in: [packages/opaque/src/client.ts:301](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L301)

ISO datetime; converted to a block (~12s/block) or slot (~400ms/slot) at call time.

***

### slotOrBlock?

> `optional` **slotOrBlock?**: `number`

Defined in: [packages/opaque/src/client.ts:299](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/client.ts#L299)

Absolute Ethereum block number or Solana slot. Takes precedence over [dateTime](#datetime).
