# Function: generateRandomMetaAddress()

> **generateRandomMetaAddress**(): `` `0x${string}` ``

Defined in: [packages/opaque/src/crypto/dksap.ts:60](https://github.com/opaquecash/sdk/blob/d653e273eb390dbec38241c20772af6021a1f8d8/packages/opaque/src/crypto/dksap.ts#L60)

A fresh random 66-byte meta-address from two throwaway private keys. The keys are
discarded — nobody can ever scan for or spend from announcements made to it. Used by
the anonymity-set utilities to mint decoy recipients (guide §17).

## Returns

`` `0x${string}` ``
