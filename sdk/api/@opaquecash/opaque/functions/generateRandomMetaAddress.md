# Function: generateRandomMetaAddress()

> **generateRandomMetaAddress**(): `` `0x${string}` ``

Defined in: [packages/opaque/src/crypto/dksap.ts:60](https://github.com/opaquecash/sdk/blob/1c668db24714147d90bc3f7ba748f59aed829f1f/packages/opaque/src/crypto/dksap.ts#L60)

A fresh random 66-byte meta-address from two throwaway private keys. The keys are
discarded — nobody can ever scan for or spend from announcements made to it. Used by
the anonymity-set utilities to mint decoy recipients (guide §17).

## Returns

`` `0x${string}` ``
