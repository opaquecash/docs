# solanaPsr

`@opaquecash/psr-chain-solana` — Solana (web3.js) PSR V2 integration: the schema registry,
attestation engine V2, and reputation-verifier proof submission. The Solana counterpart to
`@opaquecash/psr-chain` (EVM). Instruction encoding uses Anchor discriminators
(`sha256("global:<method>")`); the chain-neutral schema/attestation codecs live in
`@opaquecash/psr-core`.

## Interfaces

- [Groth16ProofInput](interfaces/Groth16ProofInput.md)
- [ParsedAttestationPda](interfaces/ParsedAttestationPda.md)
- [ParsedSchemaPda](interfaces/ParsedSchemaPda.md)
- [PsrSolanaPrograms](interfaces/PsrSolanaPrograms.md)

## Variables

- [VERIFY\_REPUTATION\_DISCRIMINATOR](variables/VERIFY_REPUTATION_DISCRIMINATOR.md)

## Functions

- [accountDiscriminator](functions/accountDiscriminator.md)
- [anchorDiscriminator](functions/anchorDiscriminator.md)
- [bigIntToBytes32](functions/bigIntToBytes32.md)
- [buildAddDelegateInstruction](functions/buildAddDelegateInstruction.md)
- [buildAttestInstruction](functions/buildAttestInstruction.md)
- [buildDeprecateSchemaInstruction](functions/buildDeprecateSchemaInstruction.md)
- [buildRegisterSchemaInstruction](functions/buildRegisterSchemaInstruction.md)
- [buildRemoveDelegateInstruction](functions/buildRemoveDelegateInstruction.md)
- [buildRevokeInstruction](functions/buildRevokeInstruction.md)
- [buildVerifyReputationInstruction](functions/buildVerifyReputationInstruction.md)
- [computeSchemaId](functions/computeSchemaId.md)
- [deriveAttestationPda](functions/deriveAttestationPda.md)
- [deriveMerkleRootPda](functions/deriveMerkleRootPda.md)
- [deriveNullifierPda](functions/deriveNullifierPda.md)
- [deriveRootHistoryPda](functions/deriveRootHistoryPda.md)
- [deriveSchemaPda](functions/deriveSchemaPda.md)
- [deriveVerifierConfigPda](functions/deriveVerifierConfigPda.md)
- [encodeGroth16Proof](functions/encodeGroth16Proof.md)
- [fetchAllAttestations](functions/fetchAllAttestations.md)
- [fetchAllSchemas](functions/fetchAllSchemas.md)
- [fetchAttestationPda](functions/fetchAttestationPda.md)
- [fetchLatestValidMerkleRoot](functions/fetchLatestValidMerkleRoot.md)
- [fetchSchemaPda](functions/fetchSchemaPda.md)
- [getPsrSolanaPrograms](functions/getPsrSolanaPrograms.md)
- [parseAttestationPda](functions/parseAttestationPda.md)
- [parseSchemaPda](functions/parseSchemaPda.md)
- [submitReputationProof](functions/submitReputationProof.md)
