# tobyjaguar

Building third-party apps for the [Foundation Passport Prime](https://foundation.xyz) hardware wallet (KeyOS).

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

## Passport Prime apps

| Repo | App |
|---|---|
| `passport-eth-wallet` | Ethereum wallet |
| `passport-ssh-agent` | SSH / Git signing agent with on-device approval |
| `passport-notarizer` | Document notarizer (SHA-256 + RFC 3161 proof bundles) |
| `passport-nostr-signer` | Nostr event signer (BIP-340) |

(Private during development; opening up as they reach the KeyOS app store.)
