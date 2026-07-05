# @opaquecash/opaque

Single entry point for Opaque **stealth** (EIP-5564) and **PSR** flows used together with your own indexer.

**Full documentation** (guides, API reference, playground): **[docs.opaque.cash](https://docs.opaque.cash)**

## Install

```bash
npm install @opaquecash/opaque
```

The package ships TypeScript types and depends on **`viem`** (v2). You must load the **WASM** bundle (`cryptography.js`) at runtime—either from your app’s static assets or a hosted URL (see below).

### Working from this repository

```bash
cd sdk && npm install && npm run build
```

Then depend on `@opaquecash/opaque` via your workspace or `npm link`.

## Initialize

```ts
import { OpaqueClient } from "@opaquecash/opaque";

const client = await OpaqueClient.create({
  chainId: 11155111,
  rpcUrl: "https://…",
  walletSignature: userSignatureHex,
  ethereumAddress: userAddress,
  wasmModuleSpecifier: new URL("/pkg/cryptography.js", import.meta.url).href,
});
```

Hosted WASM entry used by the reference app:

`https://www.opaque.cash/pkg/cryptography.js`

## Constants

- `OpaqueClient.supportedChainIds()`
- `OpaqueClient.chainDeployment(chainId)` — registry, announcer, verifier, default tokens
- `NATIVE_TOKEN_ADDRESS` — sentinel for ETH in balance aggregation

## Indexer announcements

Pass subgraph-shaped rows:

```ts
const rows: IndexerAnnouncement[] = [
  {
    blockNumber: "10533630",
    etherealPublicKey: "0x02…",
    logIndex: 161,
    metadata: "0x…",
    stealthAddress: "0x…",
    transactionHash: "0x…",
    viewTag: 234,
  },
];
```

## Flows

| Goal | API |
|------|-----|
| Resolve recipient meta-address (registry read via `rpcUrl`) | `resolveRecipientMetaAddress(normalAddress)` |
| Register meta-address calldata | `buildRegisterMetaAddressTransaction()` |
| Send: derive stealth + ephemeral | `prepareStealthSend(recipientMetaHex)` |
| Announce calldata | `buildAnnounceTransactionRequest(prepareResult)` |
| Owned outputs | `filterOwnedAnnouncements(rows)` |
| Balances by token | `getBalancesFromAnnouncements(rows)` |
| PSR traits | `discoverTraitsV2(rows, { chain })` |

You always submit transactions from your own wallet; the SDK returns **structured calldata** and **read results**.

Use `discoverTraits(rows)` only for legacy V1 `0xA7` attestation markers. Schema-bound
attestations created by `issueAttestation` use V2 `0xB2` metadata and require
`discoverTraitsV2`.

## Lower-level packages

`@opaquecash/stealth-core`, `@opaquecash/stealth-wasm`, `@opaquecash/stealth-chain`, `@opaquecash/psr-core`, and related packages remain available for advanced integrations.

`@opaquecash/opaque` — unified Opaque SDK client.

Initialize once with chain, RPC, wallet signature, and WASM URL; then prepare txs,
filter indexer announcements, aggregate balances, reconstruct one-time spend keys, and discover PSR traits.

## Namespaces

- [solanaPsr](/sdk/api/@opaquecash/opaque/namespaces/solanaPsr/README.md)

## Classes

- [EvmAdapter](/sdk/api/@opaquecash/opaque/classes/EvmAdapter.md)
- [OpaqueClient](/sdk/api/@opaquecash/opaque/classes/OpaqueClient.md)
- [SolanaAdapter](/sdk/api/@opaquecash/opaque/classes/SolanaAdapter.md)

## Interfaces

- [Announcement](/sdk/api/@opaquecash/opaque/interfaces/Announcement.md)
- [AnnouncementHandlers](/sdk/api/@opaquecash/opaque/interfaces/AnnouncementHandlers.md)
- [AnnounceTransactionRequest](/sdk/api/@opaquecash/opaque/interfaces/AnnounceTransactionRequest.md)
- [AnnounceWithRelayRequest](/sdk/api/@opaquecash/opaque/interfaces/AnnounceWithRelayRequest.md)
- [ArtifactPaths](/sdk/api/@opaquecash/opaque/interfaces/ArtifactPaths.md)
- [AttestationV2](/sdk/api/@opaquecash/opaque/interfaces/AttestationV2.md)
- [ChainAdapter](/sdk/api/@opaquecash/opaque/interfaces/ChainAdapter.md)
- [CreateSchemaParams](/sdk/api/@opaquecash/opaque/interfaces/CreateSchemaParams.md)
- [CreateSchemaResult](/sdk/api/@opaquecash/opaque/interfaces/CreateSchemaResult.md)
- [CrossChainAnnouncementRecord](/sdk/api/@opaquecash/opaque/interfaces/CrossChainAnnouncementRecord.md)
- [DiscoveredTrait](/sdk/api/@opaquecash/opaque/interfaces/DiscoveredTrait.md)
- [DiscoverTraitsV2Options](/sdk/api/@opaquecash/opaque/interfaces/DiscoverTraitsV2Options.md)
- [EvmAdapterConfig](/sdk/api/@opaquecash/opaque/interfaces/EvmAdapterConfig.md)
- [EvmAnnounceWithRelayResult](/sdk/api/@opaquecash/opaque/interfaces/EvmAnnounceWithRelayResult.md)
- [EvmUnifiedSigner](/sdk/api/@opaquecash/opaque/interfaces/EvmUnifiedSigner.md)
- [FetchAnnouncementsOptions](/sdk/api/@opaquecash/opaque/interfaces/FetchAnnouncementsOptions.md)
- [FieldDef](/sdk/api/@opaquecash/opaque/interfaces/FieldDef.md)
- [IndexerAnnouncement](/sdk/api/@opaquecash/opaque/interfaces/IndexerAnnouncement.md)
- [IssueAttestationParams](/sdk/api/@opaquecash/opaque/interfaces/IssueAttestationParams.md)
- [IssueAttestationResult](/sdk/api/@opaquecash/opaque/interfaces/IssueAttestationResult.md)
- [OpaqueChainDeployment](/sdk/api/@opaquecash/opaque/interfaces/OpaqueChainDeployment.md)
- [OpaqueClientConfig](/sdk/api/@opaquecash/opaque/interfaces/OpaqueClientConfig.md)
- [OutputBalance](/sdk/api/@opaquecash/opaque/interfaces/OutputBalance.md)
- [OwnedStealthOutput](/sdk/api/@opaquecash/opaque/interfaces/OwnedStealthOutput.md)
- [PrepareStealthSendResult](/sdk/api/@opaquecash/opaque/interfaces/PrepareStealthSendResult.md)
- [ProofData](/sdk/api/@opaquecash/opaque/interfaces/ProofData.md)
- [PsrExpiryInput](/sdk/api/@opaquecash/opaque/interfaces/PsrExpiryInput.md)
- [PsrTxResult](/sdk/api/@opaquecash/opaque/interfaces/PsrTxResult.md)
- [RegisterMetaAddressResult](/sdk/api/@opaquecash/opaque/interfaces/RegisterMetaAddressResult.md)
- [RegisterMetaAddressTransactionRequest](/sdk/api/@opaquecash/opaque/interfaces/RegisterMetaAddressTransactionRequest.md)
- [ResolvedRecipient](/sdk/api/@opaquecash/opaque/interfaces/ResolvedRecipient.md)
- [ResolveRecipientMetaResult](/sdk/api/@opaquecash/opaque/interfaces/ResolveRecipientMetaResult.md)
- [ResolveTransports](/sdk/api/@opaquecash/opaque/interfaces/ResolveTransports.md)
- [SchemaV2](/sdk/api/@opaquecash/opaque/interfaces/SchemaV2.md)
- [SendStealthPaymentParams](/sdk/api/@opaquecash/opaque/interfaces/SendStealthPaymentParams.md)
- [SendStealthPaymentResult](/sdk/api/@opaquecash/opaque/interfaces/SendStealthPaymentResult.md)
- [SolanaAdapterConfig](/sdk/api/@opaquecash/opaque/interfaces/SolanaAdapterConfig.md)
- [SolanaAnnounceWithRelayResult](/sdk/api/@opaquecash/opaque/interfaces/SolanaAnnounceWithRelayResult.md)
- [SolanaDeployment](/sdk/api/@opaquecash/opaque/interfaces/SolanaDeployment.md)
- [SolanaUnifiedSigner](/sdk/api/@opaquecash/opaque/interfaces/SolanaUnifiedSigner.md)
- [TokenBalanceSummary](/sdk/api/@opaquecash/opaque/interfaces/TokenBalanceSummary.md)
- [UabDeployment](/sdk/api/@opaquecash/opaque/interfaces/UabDeployment.md)
- [UabIndexerAnnouncement](/sdk/api/@opaquecash/opaque/interfaces/UabIndexerAnnouncement.md)
- [UabPayload](/sdk/api/@opaquecash/opaque/interfaces/UabPayload.md)
- [UnifiedOwnedOutput](/sdk/api/@opaquecash/opaque/interfaces/UnifiedOwnedOutput.md)
- [V2Attestation](/sdk/api/@opaquecash/opaque/interfaces/V2Attestation.md)
- [V2MerkleLeafPreimage](/sdk/api/@opaquecash/opaque/interfaces/V2MerkleLeafPreimage.md)
- [VerifyReputationArgs](/sdk/api/@opaquecash/opaque/interfaces/VerifyReputationArgs.md)

## Type Aliases

- [AnnounceWithRelayResult](/sdk/api/@opaquecash/opaque/type-aliases/AnnounceWithRelayResult.md)
- [AttestationField](/sdk/api/@opaquecash/opaque/type-aliases/AttestationField.md)
- [AttestationIdentifier](/sdk/api/@opaquecash/opaque/type-aliases/AttestationIdentifier.md)
- [DummyAnnouncement](/sdk/api/@opaquecash/opaque/type-aliases/DummyAnnouncement.md)
- [FieldType](/sdk/api/@opaquecash/opaque/type-aliases/FieldType.md)
- [OpaqueScanChain](/sdk/api/@opaquecash/opaque/type-aliases/OpaqueScanChain.md)
- [PrepareGhostReceiveResult](/sdk/api/@opaquecash/opaque/type-aliases/PrepareGhostReceiveResult.md)
- [ProofProgressCallback](/sdk/api/@opaquecash/opaque/type-aliases/ProofProgressCallback.md)
- [PsrChain](/sdk/api/@opaquecash/opaque/type-aliases/PsrChain.md)
- [ResolvedRecipientSource](/sdk/api/@opaquecash/opaque/type-aliases/ResolvedRecipientSource.md)
- [SolanaCluster](/sdk/api/@opaquecash/opaque/type-aliases/SolanaCluster.md)
- [UnifiedSigner](/sdk/api/@opaquecash/opaque/type-aliases/UnifiedSigner.md)

## Variables

- [CONSISTENCY\_FINALIZED](/sdk/api/@opaquecash/opaque/variables/CONSISTENCY_FINALIZED.md)
- [CONSISTENCY\_SAFE](/sdk/api/@opaquecash/opaque/variables/CONSISTENCY_SAFE.md)
- [DEFAULT\_IPFS\_GATEWAYS](/sdk/api/@opaquecash/opaque/variables/DEFAULT_IPFS_GATEWAYS.md)
- [DEFAULT\_REPUTATION\_ARTIFACT\_PATHS](/sdk/api/@opaquecash/opaque/variables/DEFAULT_REPUTATION_ARTIFACT_PATHS.md)
- [DEFAULT\_REPUTATION\_ARTIFACTS\_ORIGIN](/sdk/api/@opaquecash/opaque/variables/DEFAULT_REPUTATION_ARTIFACTS_ORIGIN.md)
- [EIP5564\_SCHEME\_SECP256K1](/sdk/api/@opaquecash/opaque/variables/EIP5564_SCHEME_SECP256K1.md)
- [META\_ADDRESS\_VALUE\_PREFIX](/sdk/api/@opaquecash/opaque/variables/META_ADDRESS_VALUE_PREFIX.md)
- [NATIVE\_TOKEN\_ADDRESS](/sdk/api/@opaquecash/opaque/variables/NATIVE_TOKEN_ADDRESS.md)
- [OPAQUE\_META\_RECORD\_KEY](/sdk/api/@opaquecash/opaque/variables/OPAQUE_META_RECORD_KEY.md)
- [SCHEMA\_VERSION](/sdk/api/@opaquecash/opaque/variables/SCHEMA_VERSION.md)
- [SETUP\_MESSAGE](/sdk/api/@opaquecash/opaque/variables/SETUP_MESSAGE.md)
- [UAB\_PAYLOAD\_LENGTH](/sdk/api/@opaquecash/opaque/variables/UAB_PAYLOAD_LENGTH.md)
- [WORMHOLE\_CHAIN\_ETHEREUM](/sdk/api/@opaquecash/opaque/variables/WORMHOLE_CHAIN_ETHEREUM.md)
- [WORMHOLE\_CHAIN\_ID](/sdk/api/@opaquecash/opaque/variables/WORMHOLE_CHAIN_ID.md)
- [WORMHOLE\_CHAIN\_SOLANA](/sdk/api/@opaquecash/opaque/variables/WORMHOLE_CHAIN_SOLANA.md)
- [WORMHOLESCAN\_MAINNET](/sdk/api/@opaquecash/opaque/variables/WORMHOLESCAN_MAINNET.md)
- [WORMHOLESCAN\_TESTNET](/sdk/api/@opaquecash/opaque/variables/WORMHOLESCAN_TESTNET.md)
- [ZERO\_ADDRESS](/sdk/api/@opaquecash/opaque/variables/ZERO_ADDRESS.md)
- [ZERO\_BYTES32](/sdk/api/@opaquecash/opaque/variables/ZERO_BYTES32.md)

## Functions

- [announcementToIndexerRow](/sdk/api/@opaquecash/opaque/functions/announcementToIndexerRow.md)
- [buildActionScope](/sdk/api/@opaquecash/opaque/functions/buildActionScope.md)
- [computeSchemaId](/sdk/api/@opaquecash/opaque/functions/computeSchemaId.md)
- [computeStealthAddressAndViewTag](/sdk/api/@opaquecash/opaque/functions/computeStealthAddressAndViewTag.md)
- [computeUid](/sdk/api/@opaquecash/opaque/functions/computeUid.md)
- [decodeAttestationData](/sdk/api/@opaquecash/opaque/functions/decodeAttestationData.md)
- [decodeUabPayload](/sdk/api/@opaquecash/opaque/functions/decodeUabPayload.md)
- [deriveKeysFromSignature](/sdk/api/@opaquecash/opaque/functions/deriveKeysFromSignature.md)
- [encodeAttestationData](/sdk/api/@opaquecash/opaque/functions/encodeAttestationData.md)
- [encodeUabPayload](/sdk/api/@opaquecash/opaque/functions/encodeUabPayload.md)
- [encodeV2AttestationMetadata](/sdk/api/@opaquecash/opaque/functions/encodeV2AttestationMetadata.md)
- [ephemeralPrivateKeyToCompressedPublicKey](/sdk/api/@opaquecash/opaque/functions/ephemeralPrivateKeyToCompressedPublicKey.md)
- [externalNullifierFromScope](/sdk/api/@opaquecash/opaque/functions/externalNullifierFromScope.md)
- [extractMetaAddressFromDidDocument](/sdk/api/@opaquecash/opaque/functions/extractMetaAddressFromDidDocument.md)
- [fetchVaa](/sdk/api/@opaquecash/opaque/functions/fetchVaa.md)
- [fieldDefsToString](/sdk/api/@opaquecash/opaque/functions/fieldDefsToString.md)
- [generateRandomMetaAddress](/sdk/api/@opaquecash/opaque/functions/generateRandomMetaAddress.md)
- [getChainDeployment](/sdk/api/@opaquecash/opaque/functions/getChainDeployment.md)
- [getSolanaDeployment](/sdk/api/@opaquecash/opaque/functions/getSolanaDeployment.md)
- [getSupportedChainIds](/sdk/api/@opaquecash/opaque/functions/getSupportedChainIds.md)
- [getUabDeployment](/sdk/api/@opaquecash/opaque/functions/getUabDeployment.md)
- [indexerAnnouncementsToScannerJson](/sdk/api/@opaquecash/opaque/functions/indexerAnnouncementsToScannerJson.md)
- [indexerAnnouncementToScannerRecord](/sdk/api/@opaquecash/opaque/functions/indexerAnnouncementToScannerRecord.md)
- [ipfsPathFromInput](/sdk/api/@opaquecash/opaque/functions/ipfsPathFromInput.md)
- [isOnsNameInput](/sdk/api/@opaquecash/opaque/functions/isOnsNameInput.md)
- [isSnsNameInput](/sdk/api/@opaquecash/opaque/functions/isSnsNameInput.md)
- [isZeroUid](/sdk/api/@opaquecash/opaque/functions/isZeroUid.md)
- [keysToStealthMetaAddress](/sdk/api/@opaquecash/opaque/functions/keysToStealthMetaAddress.md)
- [packSchemaIdToField](/sdk/api/@opaquecash/opaque/functions/packSchemaIdToField.md)
- [parseFieldDefs](/sdk/api/@opaquecash/opaque/functions/parseFieldDefs.md)
- [parseMetaAddressValue](/sdk/api/@opaquecash/opaque/functions/parseMetaAddressValue.md)
- [parseStealthMetaAddress](/sdk/api/@opaquecash/opaque/functions/parseStealthMetaAddress.md)
- [randomNonce](/sdk/api/@opaquecash/opaque/functions/randomNonce.md)
- [recipientStealthPoint](/sdk/api/@opaquecash/opaque/functions/recipientStealthPoint.md)
- [recomputeStealthSendFromEphemeralPrivateKey](/sdk/api/@opaquecash/opaque/functions/recomputeStealthSendFromEphemeralPrivateKey.md)
- [requestSetupSignature](/sdk/api/@opaquecash/opaque/functions/requestSetupSignature.md)
- [requireChainDeployment](/sdk/api/@opaquecash/opaque/functions/requireChainDeployment.md)
- [requireUabDeployment](/sdk/api/@opaquecash/opaque/functions/requireUabDeployment.md)
- [resolveEnsMetaAddress](/sdk/api/@opaquecash/opaque/functions/resolveEnsMetaAddress.md)
- [resolveIpfsDidMetaAddress](/sdk/api/@opaquecash/opaque/functions/resolveIpfsDidMetaAddress.md)
- [resolveSnsMetaAddress](/sdk/api/@opaquecash/opaque/functions/resolveSnsMetaAddress.md)
- [selectSigner](/sdk/api/@opaquecash/opaque/functions/selectSigner.md)
- [stealthMetaAddressToHex](/sdk/api/@opaquecash/opaque/functions/stealthMetaAddressToHex.md)
- [uabPayloadToMetadata](/sdk/api/@opaquecash/opaque/functions/uabPayloadToMetadata.md)
- [uabStealthAddressEvm](/sdk/api/@opaquecash/opaque/functions/uabStealthAddressEvm.md)
- [viewOnlyMetaAddress](/sdk/api/@opaquecash/opaque/functions/viewOnlyMetaAddress.md)
