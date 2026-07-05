# Function: generateRandomMetaAddress()

> **generateRandomMetaAddress**(): `` `0x${string}` ``

Defined in: [packages/opaque/src/crypto/dksap.ts:104](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L104)

A fresh random 66-byte meta-address from two throwaway private keys. The keys are
discarded — nobody can ever scan for or spend from announcements made to it. Used by
the anonymity-set utilities to mint decoy recipients (guide §17).

## Returns

`` `0x${string}` ``
