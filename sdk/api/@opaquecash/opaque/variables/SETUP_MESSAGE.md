# Variable: SETUP\_MESSAGE

> `const` **SETUP\_MESSAGE**: `"Sign this message to derive your Opaque Cash stealth keys. This does not approve any transaction."` = `"Sign this message to derive your Opaque Cash stealth keys. This does not approve any transaction."`

Defined in: [packages/opaque/src/crypto/dksap.ts:25](https://github.com/opaquecash/sdk/blob/07b81594b33091d87157623bffc2d7ba1ab07e5d/packages/opaque/src/crypto/dksap.ts#L25)

Canonical message a wallet must sign before [deriveKeysFromSignature](/sdk/api/@opaquecash/opaque/functions/deriveKeysFromSignature.md).
Chain-neutral by design — the same wallet derives the same keys everywhere.
MUST match `spec/CSAP.md` §2.2 and both frontends' `SETUP_MESSAGE` byte-for-byte.
