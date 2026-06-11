# Interface: PsrExpiryInput

Defined in: [packages/opaque/src/client.ts:268](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L268)

Future block (Ethereum) / slot (Solana) for a schema or attestation expiry.

## Properties

### dateTime?

> `optional` **dateTime?**: `string`

Defined in: [packages/opaque/src/client.ts:272](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L272)

ISO datetime; converted to a block (~12s/block) or slot (~400ms/slot) at call time.

***

### slotOrBlock?

> `optional` **slotOrBlock?**: `number`

Defined in: [packages/opaque/src/client.ts:270](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/client.ts#L270)

Absolute Ethereum block number or Solana slot. Takes precedence over [dateTime](#datetime).
