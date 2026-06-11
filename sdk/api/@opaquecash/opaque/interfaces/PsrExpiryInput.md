# Interface: PsrExpiryInput

Defined in: [packages/opaque/src/client.ts:317](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L317)

Future block (Ethereum) / slot (Solana) for a schema or attestation expiry.

## Properties

### dateTime?

> `optional` **dateTime?**: `string`

Defined in: [packages/opaque/src/client.ts:321](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L321)

ISO datetime; converted to a block (~12s/block) or slot (~400ms/slot) at call time.

***

### slotOrBlock?

> `optional` **slotOrBlock?**: `number`

Defined in: [packages/opaque/src/client.ts:319](https://github.com/opaquecash/sdk/blob/1ac32abb86be54d81add3fae49381204ea1eb7c5/packages/opaque/src/client.ts#L319)

Absolute Ethereum block number or Solana slot. Takes precedence over [dateTime](#datetime).
