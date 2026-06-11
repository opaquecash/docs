# Variable: VERIFY\_REPUTATION\_DISCRIMINATOR

> `const` **VERIFY\_REPUTATION\_DISCRIMINATOR**: `Uint8Array`

Defined in: packages/psr-chain-solana/dist/reputation.d.ts:13

`verify_reputation` instruction discriminator — Anchor's standard
`sha256("global:verify_reputation")[0..8]`, matching the V2 program deployed
2026-06-10. (The pre-V2 devnet build used a custom dispatch tag; that program
was never functional and has been upgraded.) Pass a custom value to
[buildVerifyReputationInstruction](../functions/buildVerifyReputationInstruction.md) only for non-standard builds.
