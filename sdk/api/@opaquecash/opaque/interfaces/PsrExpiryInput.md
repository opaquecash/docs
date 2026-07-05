# Interface: PsrExpiryInput

Defined in: [packages/opaque/src/client.ts:388](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L388)

Future block (Ethereum) / slot (Solana) for a schema or attestation expiry.

## Properties

### dateTime?

> `optional` **dateTime?**: `string`

Defined in: [packages/opaque/src/client.ts:392](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L392)

ISO datetime; converted to a block (~12s/block) or slot (~400ms/slot) at call time.

***

### slotOrBlock?

> `optional` **slotOrBlock?**: `number`

Defined in: [packages/opaque/src/client.ts:390](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/client.ts#L390)

Absolute Ethereum block number or Solana slot. Takes precedence over [dateTime](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md#datetime).
