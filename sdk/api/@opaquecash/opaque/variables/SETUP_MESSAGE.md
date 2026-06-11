# Variable: SETUP\_MESSAGE

> `const` **SETUP\_MESSAGE**: `"Sign this message to derive your Opaque Cash stealth keys. This does not approve any transaction."` = `"Sign this message to derive your Opaque Cash stealth keys. This does not approve any transaction."`

Defined in: [packages/opaque/src/crypto/dksap.ts:20](https://github.com/opaquecash/sdk/blob/1dd683193540a37fa1c0158af24782241086d3f9/packages/opaque/src/crypto/dksap.ts#L20)

Canonical message a wallet must sign before [deriveKeysFromSignature](../functions/deriveKeysFromSignature.md).
Chain-neutral by design — the same wallet derives the same keys everywhere.
MUST match `spec/CSAP.md` §2.2 and both frontends' `SETUP_MESSAGE` byte-for-byte.
