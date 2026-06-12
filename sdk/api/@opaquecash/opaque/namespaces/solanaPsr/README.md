# solanaPsr

`@opaquecash/psr-chain-solana` — Solana (web3.js) PSR V2 integration: the schema registry,
attestation engine V2, and reputation-verifier proof submission. The Solana counterpart to
`@opaquecash/psr-chain` (EVM). Instruction encoding uses Anchor discriminators
(`sha256("global:<method>")`); the chain-neutral schema/attestation codecs live in
`@opaquecash/psr-core`.

## Interfaces

- [Groth16ProofInput](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/interfaces/Groth16ProofInput.md)
- [ParsedAttestationPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/interfaces/ParsedAttestationPda.md)
- [ParsedSchemaPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/interfaces/ParsedSchemaPda.md)
- [PsrSolanaPrograms](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/interfaces/PsrSolanaPrograms.md)

## Variables

- [VERIFY\_REPUTATION\_DISCRIMINATOR](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/variables/VERIFY_REPUTATION_DISCRIMINATOR.md)

## Functions

- [accountDiscriminator](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/accountDiscriminator.md)
- [anchorDiscriminator](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/anchorDiscriminator.md)
- [bigIntToBytes32](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/bigIntToBytes32.md)
- [buildAddDelegateInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildAddDelegateInstruction.md)
- [buildAttestInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildAttestInstruction.md)
- [buildDeprecateSchemaInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildDeprecateSchemaInstruction.md)
- [buildRegisterSchemaInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildRegisterSchemaInstruction.md)
- [buildRemoveDelegateInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildRemoveDelegateInstruction.md)
- [buildRevokeInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildRevokeInstruction.md)
- [buildVerifyReputationInstruction](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/buildVerifyReputationInstruction.md)
- [computeSchemaId](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/computeSchemaId.md)
- [deriveAttestationPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/deriveAttestationPda.md)
- [deriveMerkleRootPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/deriveMerkleRootPda.md)
- [deriveNullifierPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/deriveNullifierPda.md)
- [deriveRootHistoryPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/deriveRootHistoryPda.md)
- [deriveSchemaPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/deriveSchemaPda.md)
- [deriveVerifierConfigPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/deriveVerifierConfigPda.md)
- [encodeGroth16Proof](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/encodeGroth16Proof.md)
- [fetchAllAttestations](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/fetchAllAttestations.md)
- [fetchAllSchemas](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/fetchAllSchemas.md)
- [fetchAttestationPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/fetchAttestationPda.md)
- [fetchLatestValidMerkleRoot](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/fetchLatestValidMerkleRoot.md)
- [fetchSchemaPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/fetchSchemaPda.md)
- [getPsrSolanaPrograms](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/getPsrSolanaPrograms.md)
- [parseAttestationPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/parseAttestationPda.md)
- [parseSchemaPda](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/parseSchemaPda.md)
- [submitReputationProof](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/functions/submitReputationProof.md)
