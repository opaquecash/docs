# Interface: PsrExpiryInput

Defined in: [packages/opaque/src/client.ts:334](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L334)

Future block (Ethereum) / slot (Solana) for a schema or attestation expiry.

## Properties

### dateTime?

> `optional` **dateTime?**: `string`

Defined in: [packages/opaque/src/client.ts:338](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L338)

ISO datetime; converted to a block (~12s/block) or slot (~400ms/slot) at call time.

***

### slotOrBlock?

> `optional` **slotOrBlock?**: `number`

Defined in: [packages/opaque/src/client.ts:336](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/client.ts#L336)

Absolute Ethereum block number or Solana slot. Takes precedence over [dateTime](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md#datetime).
