# Interface: UseStealthBalanceResult

Defined in: useStealthBalance.ts:6

State returned by [useStealthBalance](../functions/useStealthBalance.md).

## Properties

### balances

> **balances**: [`OutputBalance`](../../opaque/interfaces/OutputBalance.md)[]

Defined in: useStealthBalance.ts:8

Native balance per owned output (wei / lamports), in input order.

***

### error

> **error**: `Error` \| `null`

Defined in: useStealthBalance.ts:14

Last fetch error, cleared by the next successful fetch.

***

### loading

> **loading**: `boolean`

Defined in: useStealthBalance.ts:12

True while balances are being fetched.

***

### totals

> **totals**: `object`

Defined in: useStealthBalance.ts:10

Sum of `balances` per chain, in base units.

#### ethereum

> **ethereum**: `bigint`

#### solana

> **solana**: `bigint`
