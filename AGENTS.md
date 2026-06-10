# Opaque documentation (Mintlify)

## About

- Mintlify site for Opaque Protocol (`@opaquecash/opaque` SDK)
- Pages are MDX with YAML frontmatter; config in `docs.json`
- Remote: `https://github.com/opaquecash/mintlify-docs`

## Terminology

- **OpaqueClient** — unified SDK class; document methods, not low-level chain packages unless in utilities
- **Meta-address** — 66-byte EIP-5564 stealth meta-address
- **PSR** — Provable Stealth Reputation (schemas, attestations, ZK proofs)
- **UAB** — Universal Announcement Bus (Wormhole cross-chain)
- **WASM** — `cryptography.js` from opaque-scanner; required for scan/sweep/prove

## Style

- Active voice, second person
- Every SDK method: signature, params, return type, signer/WASM requirements, runnable example
- Link to guides for E2E flows; link to `opaquecash/spec` for protocol details
- Self-host WASM (`/pkg/cryptography.js`) — do not recommend opaque.cash CDN for production

## Content boundaries

- Document public `OpaqueClient` API and re-exported utilities
- Do not duplicate full CSAP/PSR/UAB specs — link to GitHub
- Note limitations (no ERC-20/SPL stealth sends yet, relayer required for UAB delivery)

## Local dev

```bash
mint dev
```
