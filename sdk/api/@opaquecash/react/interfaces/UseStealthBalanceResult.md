# Interface: UseStealthBalanceResult

Defined in: [useStealthBalance.ts:6](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useStealthBalance.ts#L6)

State returned by [useStealthBalance](/sdk/api/@opaquecash/react/functions/useStealthBalance.md).

## Properties

### balances

> **balances**: [`OutputBalance`](/sdk/api/@opaquecash/opaque/interfaces/OutputBalance.md)[]

Defined in: [useStealthBalance.ts:8](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useStealthBalance.ts#L8)

Native balance per owned output (wei / lamports), in input order.

***

### error

> **error**: `Error` \| `null`

Defined in: [useStealthBalance.ts:14](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useStealthBalance.ts#L14)

Last fetch error, cleared by the next successful fetch.

***

### loading

> **loading**: `boolean`

Defined in: [useStealthBalance.ts:12](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useStealthBalance.ts#L12)

True while balances are being fetched.

***

### totals

> **totals**: `object`

Defined in: [useStealthBalance.ts:10](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/react/src/useStealthBalance.ts#L10)

Sum of `balances` per chain, in base units.

#### ethereum

> **ethereum**: `bigint`

#### solana

> **solana**: `bigint`
