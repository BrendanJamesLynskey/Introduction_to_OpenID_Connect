# 🪪 Introduction to OpenID Connect

An interactive Reveal.js presentation covering **OpenID Connect (OIDC)** — the identity layer on top of OAuth 2.0. ID tokens, discovery, JWKS rotation, UserInfo, response types, logout, CIBA, SIOPv2 & Verifiable Credentials, OpenID Federation 1.0, FAPI 2.0, real-world OP quirks, and the workload-OIDC pattern (GitHub Actions → AWS without long-lived keys).

## ▶ [Open the Presentation](https://brendanjameslynskey.github.io/Introduction_to_OpenID_Connect/)

## 🪪 [Advanced companion — Advanced OpenID Connect](https://brendanjameslynskey.github.io/Advanced_OpenID_Connect/)

## 🔐 [Companion deck — Introduction to OAuth](https://brendanjameslynskey.github.io/Introduction_to_OAuth/)

---

## Contents

| # | Topic | Description |
|---|-------|-------------|
| 00 | Title | Authenticate → Issue → Validate → Trust |
| 01 | Topics | Map of identity-token, flows, federation, hardening |
| 02 | Why OIDC Exists | OAuth gives you authorisation; OIDC gives you a verified identity |
| 03 | A Brief History | 2005 → 2025 — SAML, OpenID 2.0, Connect, FAPI, Federation 1.0 |
| 04 | OIDC = OAuth + Identity Token | Side-by-side request comparison; `openid` scope, `id_token`, JWKS |
| 05 | Core Flow — Authorisation Code with `openid` | Full sequence diagram, RP ↔ OP ↔ UserInfo |
| 06 | The ID Token — Anatomy | Header / payload / signature, sample claims, `iss` / `aud` / `nonce` |
| 07 | ID Token Validation — The Checklist | The 8 must-do checks, with TS/`jose` example code |
| 08 | Discovery — `.well-known/openid-configuration` | What's in the document and why every check depends on it |
| 09 | JWKS — Public Keys & Rotation | `kid`, key rotation, cache TTLs, the silent-break failure mode |
| 10 | Scopes & UserInfo | `openid` / `profile` / `email` / `address` / `phone`, the UserInfo endpoint |
| 11 | Response Types — Code, Hybrid, Implicit | What survives in 2026 and what to never ship |
| 12 | Logout & Session Management | RP-initiated, back-channel, front-channel — when each works |
| 13 | CIBA | Decoupled auth for call centres, kiosks, smart-home & payments |
| 14 | SIOPv2 & Verifiable Credentials | Self-Issued OPs, EUDI Wallet, mDL — the wallet-era stack |
| 15 | OpenID Federation 1.0 (Sep 2024) | Trust chains for ecosystems — eIDAS 2.0, education, healthcare |
| 16 | FAPI 2.0 — Financial-Grade OIDC | PAR, sender-constrained tokens, mTLS / private_key_jwt, no-implicit |
| 17 | OIDC vs SAML — Which When | Decision rules — mobile, B2B, enterprise IdP, government |
| 18 | Real-World OPs — The Quirks | Google, Entra ID, Apple, Okta, Keycloak, ZITADEL, Cognito |
| 19 | Workload OIDC — The Modern CI/CD Pattern | GitHub Actions → AWS STS via OIDC, no long-lived keys |
| 20 | Common Bugs & Mitigations | The eight foot-guns and how each fails silently |
| 21 | Summary | Three takeaways + pointers into the OAuth / SaaS / Cloud-Security decks |

---

## Slide Controls

| Action | Key |
|--------|-----|
| Next / Previous | `→` `←` or swipe |
| Overview | `Esc` |
| Fullscreen | `F` |
| Export to PDF | Append `?print-pdf` to URL, then print |

## Technology

[Reveal.js 4.6](https://revealjs.com) · [highlight.js](https://highlightjs.org) · Playfair Display + DM Sans + JetBrains Mono · inline SVG diagrams.

Single self-contained `index.html` — no build step, no npm, no dependencies to install.

## See also

- [Advanced OpenID Connect](https://github.com/BrendanJamesLynskey/Advanced_OpenID_Connect) — the deep-end companion to this deck (FAPI 2.0, OpenID Federation 1.0, EUDI Wallet stack, workload OIDC, migration playbooks).
- [OAuth — A Gentle Primer](https://github.com/BrendanJamesLynskey/OAuth_Primer) — the no-code primer for the underlying delegated-auth model.
- [Introduction to OAuth](https://github.com/BrendanJamesLynskey/Introduction_to_OAuth) — the delegated-authorisation framework OIDC sits on top of.
- [OAuth for MCP Servers & Providers](https://github.com/BrendanJamesLynskey/OAuth_for_MCP) — the OAuth profile used by MCP, with OIDC where identity is required.
- [Introduction to Web Authentication](https://github.com/BrendanJamesLynskey/Introduction_to_Web_Authentication) — passwords, sessions, WebAuthn, MFA — the wider authentication picture.
- [Cloud_aaS_04_SaaS_Architecture](https://github.com/BrendanJamesLynskey/Cloud_aaS_04_SaaS_Architecture) — B2B identity for multi-tenant SaaS (OIDC / SAML / SCIM federation, Auth-as-a-Service).
- [Cloud_aaS_05_Cloud_Security](https://github.com/BrendanJamesLynskey/Cloud_aaS_05_Cloud_Security) — workload identity, IAM federation, and zero-trust patterns built on OIDC.
- Series hub: [Cloud `*aaS`](https://github.com/BrendanJamesLynskey/Cloud_aaS_Hub).

## References

OpenID Connect Core 1.0 · OpenID Connect Discovery 1.0 · OpenID Connect Dynamic Client Registration 1.0 · OpenID Connect RP-Initiated Logout 1.0 · OpenID Connect Back-Channel Logout 1.0 · OpenID Connect Front-Channel Logout 1.0 · OpenID Connect CIBA Core 1.0 · SIOPv2 (Self-Issued OpenID Provider v2) · OpenID for Verifiable Credentials · OpenID Federation 1.0 · FAPI 2.0 Security Profile · RFC 7519 (JWT) · RFC 7515 (JWS) · RFC 7517 (JWK) · RFC 8414 (AS Metadata) · openid.net

## License

Educational use. Code examples provided as-is.
