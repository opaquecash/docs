# Interface: V2Attestation

Defined in: packages/psr-core/dist/types.d.ts:61

Raw JSON row emitted by `scan_attestations_v2_wasm`.

## Properties

### attestation\_uid

> `readonly` **attestation\_uid**: `string`

Defined in: packages/psr-core/dist/types.d.ts:66

***

### data\_hex

> `readonly` **data\_hex**: `string`

Defined in: packages/psr-core/dist/types.d.ts:67

***

### ephemeral\_pubkey

> `readonly` **ephemeral\_pubkey**: `number`[]

Defined in: packages/psr-core/dist/types.d.ts:78

***

### is\_valid

> `readonly` **is\_valid**: `boolean`

Defined in: packages/psr-core/dist/types.d.ts:79

***

### issuer

> `readonly` **issuer**: `string`

Defined in: packages/psr-core/dist/types.d.ts:65

***

### issuer\_authorized

> `readonly` **issuer\_authorized**: `boolean`

Defined in: packages/psr-core/dist/types.d.ts:80

***

### merkle\_leaf\_preimage

> `readonly` **merkle\_leaf\_preimage**: `object`

Defined in: packages/psr-core/dist/types.d.ts:69

#### issuer\_pk\_x

> `readonly` **issuer\_pk\_x**: `string`

#### nonce\_field

> `readonly` **nonce\_field**: `string`

#### schema\_id\_field

> `readonly` **schema\_id\_field**: `string`

#### stealth\_pk\_field

> `readonly` **stealth\_pk\_field**: `string`

#### trait\_data\_hash

> `readonly` **trait\_data\_hash**: `string`

***

### nonce

> `readonly` **nonce**: `string`

Defined in: packages/psr-core/dist/types.d.ts:68

***

### schema\_id

> `readonly` **schema\_id**: `string`

Defined in: packages/psr-core/dist/types.d.ts:63

***

### schema\_name?

> `readonly` `optional` **schema\_name?**: `string` \| `null`

Defined in: packages/psr-core/dist/types.d.ts:64

***

### slot

> `readonly` **slot**: `number`

Defined in: packages/psr-core/dist/types.d.ts:77

***

### stealth\_address

> `readonly` **stealth\_address**: `string`

Defined in: packages/psr-core/dist/types.d.ts:62

***

### tx\_hash

> `readonly` **tx\_hash**: `string`

Defined in: packages/psr-core/dist/types.d.ts:76
