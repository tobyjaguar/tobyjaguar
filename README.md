# Toby Jaguar

Software engineer at [Kromeon](https://kromeon.com/), in San Diego. MSCS from NYU, MFA from UCSD.

I build in three directions that keep converging: **hardware-backed keys**, **smart contracts**, and **autonomous agents** — mostly in Go, TypeScript, and Solidity. I write about them at [tobyjaguar.com](https://tobyjaguar.com).

## Currently building

Third-party apps for the [Foundation Passport Prime](https://foundation.xyz) hardware wallet (KeyOS) — signing and wallet tooling where the private key never leaves the device.

| Repo | App |
|---|---|
| `passport-eth-wallet` | Ethereum wallet |
| `passport-ssh-agent` | SSH / Git signing agent with on-device approval |
| `passport-notarizer` | Document notarizer (SHA-256 + RFC 3161 proof bundles) |
| `passport-nostr-signer` | Nostr event signer (BIP-340) |

Private during development; opening up as they reach the KeyOS app store. Everything I publish there is signed with the [publisher key below](#keyos-publisher-identity).

## Selected work

**Agents & simulation**

- [Synjury](https://synjury.xyz) — decentralized AI-jury arbitration for the agentic economy: when agents transacting over x402 / AP2 rails hit a dispute, a panel of independent models from different families weighs the evidence and returns a verdict that settles the on-chain escrow
- [mini-world](https://github.com/tobyjaguar/mini-world) — [CrossWorlds](https://crossworlds.xyz), a persistent autonomous world simulation that runs 24/7 (Go)
- [clawclubs](https://github.com/tobyjaguar/clawclubs) — an agent-first messaging hub: AI agents connect and exchange messages in shared clubs (Go)
- [sacred-texts-rag](https://github.com/tobyjaguar/sacred-texts-rag) — turns a sacred-texts.com mirror into a RAG-ready text + vector corpus (Python)

**Bitcoin**

- [ctv-mutinynet](https://github.com/tobyjaguar/ctv-mutinynet) — BitVault, a minimal `OP_CHECKTEMPLATEVERIFY` vault demo on Mutinynet (TypeScript)

**Ethereum & smart contracts**

- [smartpiggies](https://github.com/smartpiggies/smartpiggies) — an open source peer-to-peer standard for a global derivatives market
- [TimeNFTs](https://github.com/tobyjaguar/TimeNFTs) — a dynamic, time-based NFT (Solidity)
- [Uniswap-V3-APIs](https://github.com/tobyjaguar/Uniswap-V3-APIs) — token pricing service over Uniswap's V3 subgraph (Python)
- [ethereum-signed-messages](https://github.com/tobyjaguar/ethereum-signed-messages) — helpers for signing and verifying Ethereum messages

**Web & tooling**

- [wasm-chat](https://github.com/tobyjaguar/wasm-chat) — browser-based encrypted chat over WASM
- [burrito-shop](https://github.com/tobyjaguar/burrito-shop) — point-of-sale APIs for my burrito shop (TypeScript)
- [node-utilities](https://github.com/tobyjaguar/node-utilities) — a collection of handy Node helpers

More, including Klawpheus and CrossWorlds, on the [projects page](https://tobyjaguar.com/projects/).

## Writing

- [AI Agents are your new threat model](https://tobyjaguar.com/ai-agents-are-your-new-threat-model/)
- [DeFi means democratizing finance](https://tobyjaguar.com/defi-means-democratizing-finance/)
- [Pinata and NextJS APIs](https://tobyjaguar.com/pinata-and-nextjs-apis/)

## KeyOS publisher identity

Apps I publish for Passport Prime are signed with the publisher key below. Before allowing this publisher on your device (`foundation cert install` or Settings), verify that the fingerprint the device shows you **matches this one exactly**:

```
b5df4739d8c9e8fce8ff7d2a479a6dc6b7dada3704fd394853221cfc410de249
```

Short form: `b5df4739…410de249`

| | |
|---|---|
| Publisher | `tobyjaguar` |
| Contact | tobyjaguar@pm.me |
| Compressed secp256k1 public key | `035ba1c05b6d38e6c0324ba678be1c525ae3c51f16d054b169452537f410335bdb` |
| X.509 certificate | [`tobyjaguar.crt`](./tobyjaguar.crt) (valid 2026-08-11 → 2036-08-08) |

The fingerprint is the SHA-256 digest of the compressed public key. You can recompute it from [`public.pub`](./public.pub), or from the certificate with:

```bash
foundation cert fingerprint tobyjaguar.crt
```

A matching publisher *name* is not sufficient — only the fingerprint identifies the key. If a device or bundle shows a different fingerprint for "tobyjaguar", do not allow it.

## Elsewhere

[tobyjaguar.com](https://tobyjaguar.com) · [tobyjaguar@pm.me](mailto:tobyjaguar@pm.me)
