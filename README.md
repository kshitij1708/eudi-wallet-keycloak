# EUDI Keycloak Plugin

**Open-source Keycloak extension for the European Digital Identity (EUDI) Wallet**
*Aligning with eIDAS 2.0 for interoperable, privacy-preserving digital identity in Europe*

---

## 📖 Overview

The **EUDI Keycloak Plugin** integrates **Keycloak** with the upcoming **European Digital Identity (EUDI) Wallet**, enabling organizations to authenticate users and issue credentials based on EU digital identity standards.
🔗 Repository: github.com/kshitij1708/eudi-wallet-keycloak
🔗 EUDI Wallet Info (EU): European Commission — EUDI
🔑 **Key Features (MVP & Roadmap):**

* **OID4VP Support** → Authenticate users with verifiable presentations from the EUDI Wallet.
* **SD-JWT VCs** → Validate selective disclosure credentials for privacy-preserving identity proofing.
* **OID4VCI (Planned)** → Issue credentials from Keycloak directly to EUDI Wallets.
* **Trust Management** → Align with EU trusted lists and DID methods.
* **Keycloak Integration** → Works as an Authenticator SPI and Protocol Mapper.

---

## 🌍 Why This Matters

The **EUDI Wallet** (mandated by **eIDAS 2.0**) will be rolled out by EU Member States by **2026**, offering every citizen and business a secure, interoperable digital wallet. This plugin helps organizations **get ready early** by integrating wallet-based login and credential issuance into existing identity systems.

**Benefits:**

* Future-proof authentication aligned with EU regulation.
* Privacy-first login with minimal data disclosure.
* Easy adoption in Keycloak-powered infrastructures.
* Open-source and enterprise-friendly (Apache-2.0 licensed).

---

## 🚀 Quick Start

```bash
# Clone repo
git clone https://github.com/<your-org>/keycloak-eudi.git
cd keycloak-eudi

# Build plugin
mvn clean install

# Copy into Keycloak
cp target/keycloak-eudi.jar $KEYCLOAK_HOME/providers/

# Start Keycloak with plugin
docker compose up
```

Run the sample RP from `examples/sample-rp` to test wallet login flows.

---

## 🏗 Architecture

```
RP App  ──▶ Keycloak Realm
          └─▶ EUDI Verifier (Authenticator SPI)
                ├─ OID4VP Request Builder
                ├─ QR / Deep Link UI
                ├─ VP Token Validation (SD-JWT)
                ├─ Trust Policy Resolver
                └─ Attribute Mapper → KC Claims

(Planned) Issuer Provider (OID4VCI)
```

---

## 📅 Roadmap

* **M1 — Verifier MVP**: OID4VP login, SD-JWT validation, protocol mapper.
* **M2 — Admin UX**: Policy configuration, trust sources, mapping UI.
* **M3 — Issuer Beta**: OID4VCI credential issuance support.
* **M4 — Trust & Federation**: EU trust list ingestion, DID resolution.

See full [ROADMAP.md](docs/ROADMAP.md).

---

## 🔒 Security & Privacy

* Minimal disclosure with SD-JWT.
* Replay protection with nonce + audience checks.
* Configurable trust anchors (EU trust lists).
* Ephemeral handling of PII by default.

---

## 📜 License

Licensed under the **Apache License 2.0**. See [LICENSE](LICENSE).

---

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## 📌 Keywords

`keycloak` · `eudi-wallet` · `digital-identity` · `eidas2` · `oid4vp` · `oid4vci` · `verifiable-credentials` · `sd-jwt` · `ssi` · `openid`

---

## 📧 Contact

For questions, discussions, or collaboration, please open an issue or start a discussion in this repo.
